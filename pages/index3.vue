<template>
<!-- <v-carousel cycle :interval="5500" hide-delimiters show-arrows="hover" height="520" class="mx-auto">
<v-carousel-item  v-for="index in Math.ceil(daftar_ksm.data.length / 6)" :key="index"> -->
    <!-- {{ tampungksm.data.length }} -->
    <!-- <v-row align="center" justify="center" dense >
        <v-col align="center"          
        v-for= "(daf , i) in tampungksm.data" 
                :key= "i"
            
                cols="12"
                md="4"
            >
             -->
            <v-card variant="tonal"
                    width="230"
                    height="530"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/paru.jpeg"></v-img>
                {{ tampungKSM }}
                <!-- <v-card-title align="center">
                    <h3>{{ tampungksm.data[i].Nama_ksm }}</h3>
                </v-card-title>
                <v-divider></v-divider>
                <v-card-text align="center">
                    <v-sheet align="center">
                        <v-img height="70" src="/public/logorole/spv.png"></v-img>
                        <h3 align="center">Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet>
                        <v-img height="70" src="/public/logorole/chief.png"></v-img>
                        <h3 align="center">Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet>
                        <v-img height="70" src="/public/logorole/jaga2.png"></v-img>
                        <h3 align="center">Dr. Syaifulloh</h3>
                    </v-sheet>
                </v-card-text> -->
            </v-card>
        <!-- </v-col>

        
</v-row> -->

<!-- 
</v-carousel-item>
</v-carousel> -->
</template>

<script setup>

import { useNow, useDateFormat } from '@vueuse/core'    
const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    

const _dataKSM = await $fetch(`https://satu.dev.rssa.id/items/daftar_ksm`);
const dataKSM = _dataKSM.data;
const _Users = await useFetch(`http://127.0.0.1:8000/api/getUsers`);
const data = _Users.data;
// const dataPPI = _dataPPI.data;
const _jdwlDokter = await $fetch(`https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?fields=id,Nama_petugas,Ksm,Level.Nama_level_igd,Jaga_awal,Jaga_akhir`);
const jdwlDokters = _jdwlDokter.data;

let tampungKSM = [];
const ksm = _dataKSM.data
ksm.forEach(_ksm => {
    let idksm = _ksm['id'];

    let filterjdwl = jdwlDokters.filter(jadwal=>jadwal['Ksm']===idksm);
    if(filterjdwl && filterjdwl.length>0){
        let tampiljadwalBaru={
            idksm: _ksm['id'],
            ket_ksm:_ksm['Nama_ksm'],
            jadwal:[]
    };
    filterjdwl.forEach(jdwl=>{
        tampiljadwalBaru.jadwal.push(jdwl);
    });
    tampungKSM.push(tampiljadwalBaru);
    };
});
</script>