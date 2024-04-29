
  <template>
    <v-carousel height="100%" cycle :interval="5000" hide-delimiters>        
        
        <v-carousel-item class="bg-light-green-accent-2 text-center">
                
            <v-row class="mt-5 ml-5 mr-5">

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            EMERGENSI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            BEDAH UMUM
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            BEDAH PLASTIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

            </v-row>

            <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            BEDAH SARAF
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div>
                            DOKTER UMUM / KOMPLEMENTER
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            FORENSIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

            <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            GIGI DAN MULUT
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            JANTUNG
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
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
                        <div>
                            KESEHATAN ANAK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            KULIT DAN KELAMIN
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            MATA
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                </v-row>

                <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            MIKROBIOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div>
                            OBG
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            ORTHOPAEDI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
                </v-row>

                <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            PARASITOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            PARU
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
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
                        <div>
                            RADIOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            RADIOTERAPI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            REHAP MEDIK
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                </v-row>

                <v-row class="ml-5 mr-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            SARAF
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="235">
                        <div>
                            THT
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            UROLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>
                </v-row>

                <v-row class="ml-5 mr-5 mb-5">
                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            PATOLOGI
                        </div>
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="235">
                        <div>
                            ANASTESIOLOGI & TERAPI INTENSIF
                        </div>
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