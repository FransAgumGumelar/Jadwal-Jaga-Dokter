<template>

<v-row justify="center" v-for="(bebas, i) in tampungKSM" :key= "i" dense>
            <v-col align="center"  dense>
              
                <v-card variant="tonal" width="250" height="570px" class="bg-grey"> 

                  <!-- Nama KSM -->
                    <v-sheet  align="center"  height="75px" class="bg-red" >
                        <h2 align="center">
                          {{ bebas.ket_ksm }}
                        </h2>
                    </v-sheet>

                    <v-card-text v-for="(jadwal, indexJadwal) in bebas.jadwal" :key="indexJadwal">
                        <v-sheet v-if="new Date() >= new Date(jadwal.Jaga_awal) && new Date() <= new Date(jadwal.Jaga_akhir)">
                              
                            <v-sheet-item class="mt-2">
                                <h2>{{ jadwal.Level.Nama_level_igd }}</h2>
                            </v-sheet-item>
                            <v-sheet-item class="mt-2">
                                {{ jadwal.Nama_petugas }}
                            </v-sheet-item>

                        </v-sheet>
                    </v-card-text>
            
                </v-card>
            </v-col>
        </v-row>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

// ____________________________________________________________________
const waktuSekarang = ref({
  tanggal: new Date().getDate(),
  bulan: new Date().getMonth() + 1, // Bulan dimulai dari 0, jadi tambahkan 1
  tahun: new Date().getFullYear(),
  jam: new Date().getHours(),
  menit: new Date().getMinutes(),
  detik: new Date().getSeconds(),
});

const formatDuaDigit = (nilai) => (nilai <= 9 ? `0${nilai}` : nilai);

const updateWaktu = () => {
  const sekarang = new Date();
  waktuSekarang.value.tanggal = formatDuaDigit(sekarang.getDate());
  waktuSekarang.value.bulan = formatDuaDigit(sekarang.getMonth() + 1);
  waktuSekarang.value.tahun = sekarang.getFullYear();
  waktuSekarang.value.jam = formatDuaDigit(sekarang.getHours());
  waktuSekarang.value.menit = formatDuaDigit(sekarang.getMinutes());
  waktuSekarang.value.detik = formatDuaDigit(sekarang.getSeconds());
};

let waktuIntervalId;
onMounted(() => {
  waktuIntervalId = setInterval(updateWaktu, 1000);
});

onUnmounted(() => {
  clearInterval(waktuIntervalId);
});

// const _dataKSM = await $fetch(`https://satu.dev.rssa.id/items/daftar_ksm`);
// const dataKSM = _dataKSM.data;

// const _jdwlDokter = await $fetch(`https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir`);
const tanggalSekarang = new Date();
const tanggalKemarin = new Date(
  tanggalSekarang.getFullYear(),
  tanggalSekarang.getMonth(),
  tanggalSekarang.getDate() - 7
)
  .toISOString()
  .split("T")[0];
const tanggalBesok = new Date(
  tanggalSekarang.getFullYear(),
  tanggalSekarang.getMonth(),
  tanggalSekarang.getDate() + 7
)
  .toISOString()
  .split("T")[0];

// const _jdwlDokter = await $fetch(`https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir&filter[Jaga_awal][_between]=[${tanggalKemarin}, ${tanggalBesok}]`);
// const _jdwlDokter = await $fetch(`https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir&filter[Jaga_awal][_between]=[${tanggalKemarin.toISOString().split('T')[0]}, ${tanggalSekarang.toISOString().split('T')[0]}]`);
// const jdwlDokters = _jdwlDokter.data;

let tampungKSM = ref([]);
const updateKSM = async () => {
  console.log("ini refresh");
  tampungKSM.value = []; // Kosongkan array sebelum mengisi ulang
  const _dataKSM = await $fetch(`https://satu.dev.rssa.id/items/daftar_ksm`);
  const ksm = _dataKSM.data;
  const _jdwlDokter = await $fetch(
    `https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir&filter[Jaga_awal][_between]=[${tanggalKemarin}, ${tanggalBesok}]`
  );
  const jdwlDokters = _jdwlDokter.data;

  ksm.forEach((_ksm) => {
    let idksm = _ksm["id"];

    let filterjdwl = jdwlDokters.filter((jadwal) => jadwal["Ksm"] === idksm);
    if (filterjdwl && filterjdwl.length > 0) {
      let tampiljadwalBaru = {
        idksm: _ksm["id"],
        ket_ksm: _ksm["Nama_ksm"],
        jadwal: [],
      };
      const sekarang = new Date();
      filterjdwl.forEach((jdwl) => {
        const awal = new Date(jdwl.Jaga_awal);
        const akhir = new Date(jdwl.Jaga_akhir);
        if (sekarang >= awal && sekarang <= akhir) {
          tampiljadwalBaru.jadwal.push(jdwl);
        }
      });
      if (tampiljadwalBaru.jadwal.length > 0) {
        tampungKSM.value.push(tampiljadwalBaru);
      }
    }
  });
  setTimeout(updateKSM, 20000); // Jadwalkan pembaruan berikutnya setiap 10 detik
};

updateKSM(); // Panggilan awal untuk memulai proses

async function fetch(binding) {
  Swal.fire({
    position: "center",
    icon: "success",
    title: binding,
    showConfirmButton: false,
    timer: 2000,
  });
}
</script>

<style scoped>
h1 {
  margin-bottom: 15px;
}

#container {
  padding: 10px;
}

p {
  margin: 20px 0px 20px 0px;
}
</style>
