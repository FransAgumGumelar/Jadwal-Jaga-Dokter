
  <template>
    <v-carousel height="100%" cycle :interval="5000" hide-delimiters>        
        
        <v-carousel-item class="bg-light-green-accent-2 text-center">
                
            <v-row class="mt-5 ml-5 mr-5">

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div class="font-weight-black">
                            EMERGENSI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            BEDAH UMUM
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            BEDAH PLASTIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

            </v-row>

            <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            BEDAH SARAF
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div div class="font-weight-black">
                            DOKTER UMUM / KOMPLEMENTER
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            FORENSIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

            <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            GIGI DAN MULUT
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            JANTUNG
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            JIWA
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

        </v-carousel-item>

            <v-carousel-item
            class="bg-light-blue-accent-2 text-center"
            >

            <v-row class="mt-5 ml-5 mr-5">

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            KESEHATAN ANAK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            KULIT DAN KELAMIN
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            MATA
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                </v-row>

                <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            MIKROBIOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div div class="font-weight-black">
                            OBG
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            ORTHOPAEDI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
                </v-row>

                <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            PARASITOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            PARU
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            PENYAKIT DALAM
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
                </v-row>

            </v-carousel-item>

            <v-carousel-item
            class="bg-purple-lighten-2 text-center"
            >

            <v-row class="mt-5 ml-5 mr-5">

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            RADIOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            RADIOTERAPI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            REHAP MEDIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                </v-row>

                <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            SARAF
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div div class="font-weight-black">
                            THT
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            UROLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
                </v-row>

                <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            PATOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div div class="font-weight-black">
                            ANASTESIOLOGI & TERAPI INTENSIF
                        </div>
                        {{ data }}
                        {{ data }}
                        {{ data }}
                    </v-card>
                </v-col>

            </v-row>


            </v-carousel-item>
        </v-carousel>


</template>



<script setup lang="ts">
    import { useNow, useDateFormat } from '@vueuse/core'
    const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})

    const data = await useFetch('https://satu.dev.rssa.id/items/Jadwal_jaga_Dokter/11')
    

</script>