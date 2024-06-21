<template>
    
    <!-- {{ tampungKSM }} -->
    <div align="center" mb="50" class="bg-red">
            <h1> JADWAL JAGA DOKTER IGD </h1>
        </div>

    <div align="center" mb="50">
            <h1> <jam /> </h1>
        </div>
    
    <!-- {{ datajadwal }} -->
    
    <split-carousel cycle :interval="10000" height="600px" hide-delimiters>
      <div class="d-flex flex-no-wrap justify-space-between">
      <split-carousel-item v-for="(bebas, i) in tampungKSM" :key= "i" dense>
        
        <v-row align="center" justify="center" dense>
            <v-col align="center" cols="12" md="2" dense>
              
                <v-card variant="tonal" width="250" height="570px" class="bg-grey"> 

                  <!-- Nama KSM -->
                    <v-sheet  align="center"  height="75px" class="bg-red" >
                        <h2 align="center">
                          {{ bebas.ket_ksm }}
                        </h2>
                    </v-sheet>

                    <v-card-text v-for="(jadwal, indexJadwal) in bebas.jadwal" :key="indexJadwal">
                        <v-sheet v-if="new Date() >= new Date(jadwal.Tanggal_awal) && new Date() <= new Date(jadwal.Tanggal_akhir)">
                              
                            <v-sheet-item class="mt-2">
                                <h2>{{ jadwal.Tingkat_supervisi }}</h2>
                            </v-sheet-item>
                            <v-sheet-item class="mt-2">
                                {{ jadwal.Dokter_jaga }}
                            </v-sheet-item>
                            <v-sheet-item class="mt-2">
                                {{ jadwal.Tanggal_awal }}
                            </v-sheet-item>
                            <v-sheet-item class="mt-2">
                                {{ jadwal.Tanggal_akhir }}
                            </v-sheet-item>


                        </v-sheet>
                    </v-card-text>
            
                </v-card>
            </v-col>
        </v-row>
      
      </split-carousel-item>
    </div>
    </split-carousel>

  

  <v-footer class="bg-black">
      <v-row justify="center" no-gutters>
        <v-col class="text-center mt-4" cols="12">
          {{ new Date().getFullYear() }} — <strong>RSUD DR DSIFUL ANWAR</strong>
        </v-col>
      </v-row>
  </v-footer>
</template>


<script >
import { SplitCarousel, SplitCarouselItem } from "vue-split-carousel";
  export default {
    components: {
      SplitCarousel,
      SplitCarouselItem
    }
  };

  // const app = Vue.createApp({
  //   template:`
  //     <split-carousel>n
  //       <split-carousel-item v-for="i in 8">{{i}}</split-carousel-item>
  //     </split-carousel>
  //   `
  // })
  // app.use(window['vue-split-carousel'])
  // app.mount('#app')

  </script>
<script setup>




//  const datajadwal = await useFetch('https://satu.rssa.top/items/data_jadwal_jaga_igd');

  import { ref, onMounted, onUnmounted } from "vue";
  
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
  
  // let waktuIntervalId;
  // onMounted(() => {
  //   waktuIntervalId = setInterval(updateWaktu, 1000);
  // });
  
  // onUnmounted(() => {
  //   clearInterval(waktuIntervalId);
  // });
  
  
  
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
  
 
  
  let tampungKSM = ref([]);
  const updateKSM = async () => {
    console.log("ini refresh");
    tampungKSM.value = []; // Kosongkan array sebelum mengisi ulang
    // const _dataKSM = await $fetch(`https://satu.dev.rssa.id/items/daftar_ksm`);
    // const ksm = _dataKSM.data;

    // const _jdwlDokter = await $fetch(`https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir&filter[Jaga_awal][_between]=[${tanggalKemarin}, ${tanggalBesok}]`);
    // const jdwlDokters = _jdwlDokter.data;

    // const _jdwlDokter = await $fetch(`https://satu.rssa.top/items/data_jadwal_jaga_igd?fields=id,Dokter_Jaga,Ksm,Tingkat_supervisi,Tanggal_awal,Tanggal_akhir&filter[Tanggal_awal][_between]=[${tanggalKemarin}, ${tanggalBesok}]`);
    // const jdwlDokters = _jdwlDokter.data;
  
    const _dataKSM = await $fetch('https://satu.rssa.top/items/daftar_ksm');
  const ksm = _dataKSM.data;
  const _jdwlDokter = await $fetch(
    'https://satu.rssa.top/items/data_jadwal_jaga_igd?fields=id,Dokter_jaga,KSM,Tingkat_supervisi,Tanggal_awal,Tanggal_akhir,Nama_dpjp.Gelar_belakang.daftar_gelar_belakang_id,Nama_dpjp.Gelar_depan.daftar_gelar_depan_id,Nama_dpjp.KTP.Nama_lengkap&filter[Tanggal_awal][_between]=[${tanggalKemarin}, ${tanggalBesok}]'
  );

  const jdwlDokters = _jdwlDokter.data;


    ksm.forEach((_ksm) => {
      let idksm = _ksm["id"];
  
      let filterjdwl = jdwlDokters.filter((jadwal) => jadwal["KSM"] === idksm);
      if (filterjdwl && filterjdwl.length > 0) {
        let tampiljadwalBaru = {
          idksm: _ksm["id"],
          ket_ksm: _ksm["Nama_ksm"],
          jadwal: [],
        };
        const sekarang = new Date();
        filterjdwl.forEach((jdwl) => {
          const awal = new Date(jdwl.Tanggal_awal);
          const akhir = new Date(jdwl.Tanggal_akhir);
          if (sekarang >= awal && sekarang <= akhir) {
            tampiljadwalBaru.jadwal.push(jdwl);
          }
        });
        if (tampiljadwalBaru.jadwal.length > 0) {
          tampungKSM.value.push(tampiljadwalBaru);
        }
      }
    });
    setTimeout(updateKSM, 60000); // Jadwalkan pembaruan berikutnya setiap 10 detik
  };
  
  updateKSM(); // Panggilan awal untuk memulai proses
  
  // async function fetch(binding) {
  //   Swal.fire({
  //     position: "center",
  //     icon: "success",
  //     title: binding,
  //     showConfirmButton: false,
  //     timer: 2000,
  //   });
  // }
  </script>

