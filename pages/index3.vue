<template>
    
    <!-- {{ tampungKSM }} -->
    <div align="center" mb="50" class="bg-red">
            <h1> JADWAL JAGA DOKTER IGD </h1>
        </div>

    <div align="center" mb="50">
            <h1> <jam /> </h1>
        </div>
    
    
    
    <split-carousel height="500px" >
      <split-carousel-item v-for="(bebas, i) in tampungKSM" :key= "i" height="100px">
        
        <v-row>
            <v-col align="center" cols="13">
              
                <v-card variant="tonal" width="250" height="470px" color="surface-variant" class="bg-grey"> 

                  <!-- Nama KSM -->
                    <v-sheet  align="center"  height="75px" class="bg-red" no-gutters>
                        <h2 align="center">
                          {{ bebas.ket_ksm }}
                        </h2>
                        
                        
                        
                    </v-sheet>

                    <v-card-text 
                    height="100px"
                        v-for="(jadwal, indexJadwal) in bebas.jadwal"
                        :key="indexJadwal">
                        <v-sheet height="80px" v-if="new Date() >= new Date(jadwal.Jaga_awal) && new Date() <= new Date(jadwal.Jaga_akhir)">
                              
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
      </split-carousel-item>
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
  //     <split-carousel>
  //       <split-carousel-item v-for="i in 8">{{i}}</split-carousel-item>
  //     </split-carousel>
  //   `
  // })
  // app.use(window['vue-split-carousel'])
  // app.mount('#app')

  </script>
<script setup>




// const { data: daftar_ksm, } = await useFetch(() => 'https://satu.dev.rssa.id/items/daftar_ksm');

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

