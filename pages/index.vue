<template>

<v-carousel cycle :interval="5500" hide-delimiters show-arrows="hover" height="520">
<v-carousel-item>
<div class="d-flex flex-no-wrap justify-space-between">
<v-row align="center" justify="center" dense>
    <v-col>
    <v-container>
    <v-card variant="tonal"
            
            width="195"
            height="1000"
            color="surface-variant"
            > 
        <v-img height="90" src="/public/logoksm/paru.jpeg">
        </v-img>
        <v-card-title align="center">
            <h1>{{ data }}</h1>
        </v-card-title>

        <v-card-text>
            <v-container class="bg-surface-variant">
                <v-row no-gutters >
                    <v-col cols="12"sm="4" >
                        <v-sheet height="95" width="130" align="center">
                            <v-img height="50" src="/public/logorole/spv.png"></v-img>
                            <h3 align="center">Dr. Syaifulloh</h3>
                        </v-sheet>
                        <v-sheet height="95" width="130">
                            <v-img height="50" src="/public/logorole/spv.png"></v-img>
                            <h3 align="center">Dr. Syaifulloh</h3>
                        </v-sheet>
                        <v-sheet height="95" width="130">
                            <v-img height="50" src="/public/logorole/spv.png"></v-img>
                            <h3 align="center">Dr. Syaifulloh</h3>
                        </v-sheet>
                    </v-col>
                </v-row>
            </v-container>
        </v-card-text>
    </v-card>
</v-container>
</v-col>
<v-col>
    <v-container>
    <v-card variant="tonal"
    
    width="195"
              height="1000"
              color="surface-variant"
              
              > 
        <v-img height="100" src="/public/logoksm/Anastesiologi & Terapi Intensif.png">
        </v-img>
        <v-card-title align="center">
            <h1>ANASTESI</h1>
        </v-card-title>

        <v-card-text>
            <v-container class="bg-surface-variant">
                <v-row no-gutters>
                <v-col cols="12"sm="4">
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                </v-col>
                </v-row>
            </v-container>
        </v-card-text>
    </v-card>
</v-container>
</v-col>
<v-col>
    <v-container>
    <v-card variant="tonal"
    
    width="195"
              height="1000"
              color="surface-variant"> 
        <v-img height="100" src="/public/logoksm/ipd.jpg">
        </v-img>
        <v-card-title align="center">
            <h1>IPD</h1>
        </v-card-title>

        <v-card-text>
            <v-container class="bg-surface-variant">
                <v-row no-gutters>
                <v-col cols="12"sm="4">
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                </v-col>
                </v-row>
            </v-container>
        </v-card-text>
    </v-card>
</v-container>
</v-col>
<v-col>
    <v-container>
    <v-card variant="tonal"
    
    width="195"
              height="1000"
              color="surface-variant"> 
        <v-img height="100" src="/public/logoksm/ortho.jpg">
        </v-img>
        <v-card-title align="center">
            <h1>ORTHO</h1>
        </v-card-title>

        <v-card-text>
            <v-container class="bg-surface-variant">
                <v-row no-gutters>
                <v-col cols="12"sm="4">
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                </v-col>
                </v-row>
            </v-container>
        </v-card-text>
    </v-card>
</v-container>
</v-col>
<v-col>
    <v-container>
    <v-card variant="tonal"
    
    width="195"
              height="1000"
              color="surface-variant"> 
        <v-img height="100" src="/public/logoksm/paru.jpeg">
        </v-img>
        <v-card-title align="center">
            <h1>PARU</h1>
        </v-card-title>

        <v-card-text>
            <v-container class="bg-surface-variant">
                <v-row no-gutters>
                <v-col cols="12"sm="4">
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                    </v-sheet>
                    <v-sheet height="65" width="130">
                        <h2>JAGA 1</h2>
                        <h3>Dr. Syaifulloh</h3>
                        
                    </v-sheet>
                </v-col>
                <p> {{ data.data[0].Nama_ksm }} </p>
                </v-row>
            </v-container>
        </v-card-text>
    </v-card>
</v-container>
</v-col>






</v-row>
</div>



</v-carousel-item>




</v-carousel>

</template>

<script setup lang="ts">
const { data } = await useFetch('https://satu.dev.rssa.id/items/daftar_ksm?filter[id][_eq]=1')


</script>