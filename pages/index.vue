
  <template>
    <h1>index</h1>
    <v-carousel height="850" :interval="150000">        
        <v-carousel-item class="bg-light-green-accent-2 text-center">
                
            <v-row >
                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

            <v-row >
                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

            <v-row class="mt-20">
                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                        
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>

                <v-col cols="12" md="4" >
                    <v-card height="250">
                        {{ data }}
                    </v-card>
                </v-col>
            </v-row>

        </v-carousel-item>

            <v-carousel-item
            class="bg-light-blue-accent-2 text-center"
            >
            </v-carousel-item>

            <v-carousel-item
            class="bg-purple-lighten-2 text-center"
            >
            </v-carousel-item>
        </v-carousel>


</template>



<script setup lang="ts">
    import { useNow, useDateFormat } from '@vueuse/core'
    const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})

    const data = await useFetch('https://satu.dev.rssa.id/items/Jadwal_jaga_Dokter/11')
    

</script>