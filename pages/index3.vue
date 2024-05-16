<template>
<v-carousel cycle :interval="5000" hide-delimiters show-arrows="hover" height="520" class="mx-auto">
<v-carousel-item>
    <!-- {{ tampungksm.data.length }} -->
    <v-row align="center" justify="center" dense >
        <v-col align="center"          
                v-for= "i in tampungksm.data" 
                :key= "i"
            
                cols="12"
                md="4"
            >
            
            <v-card variant="tonal"
                    width="230"
                    height="530"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/paru.jpeg"></v-img>
                
                <v-card-title align="center">
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
                </v-card-text>
            </v-card>
        </v-col>

        
</v-row>


</v-carousel-item>
</v-carousel>
</template>

<script setup>

import { useNow, useDateFormat } from '@vueuse/core'    
const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    

const ksmcoba = await useFetch ('https://satu.dev.rssa.id/items/daftar_ksm')
const tampungksm = ksmcoba.data





</script>