<template>
    HALAMAN INDEX
    <container>
        <div align="center" mb="50">
            <h1> <jam /> </h1>
        </div>
    </container>



<!-- <v-carousel cycle :interval="5000" hide-delimiters show-arrows="hover">
    <v-carousel-item> -->
        <v-row>
            <v-col align="center"          
                        v-for= "(daftar , i) in ksm.data" 
                        :key= "i"
                        cols="13"
                    >
                    
                <v-card variant="tonal"
                        width="230"
                        height="auto"
                        color="surface-variant"
                        > 
                    <!-- <v-img height="150" src="/public/logoksm/paru.jpeg"></v-img> -->
                        
                    <v-card-title align="center">
                        <h3>{{ ksm.data[i].Nama_ksm }}</h3>
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
    <!-- </v-carousel-item>v-slide-group-item>
</v-carousel> -->
</template>

<!-- <template>
<v-container>  
        
        <div class="text-h4 " align="center"> 
            {{ now }}
        </div>
        
</v-container>

<v-carousel cycle :interval="5000" hide-delimiters show-arrows="hover" height="520">
<v-carousel-item>

    <v-row align="center" dense>
        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/Anastesiologi & Terapi Intensif.png"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[0].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/bedahplastik.jpg"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[1].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/bedahsaraf.png"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[2].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/bedahumum.png"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[3].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/dokterumum.png"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[4].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/emergency.jpg"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[5].Nama_ksm }}</h3>
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

        <v-col align="center">
            <v-card variant="tonal"
                    width="230"
                    height="1000"
                    color="surface-variant"
                    > 
                <v-img height="150" src="/public/logoksm/forensik.jpg"></v-img>
                
                <v-card-title align="center">
                    <h3>{{ ksm.data[6].Nama_ksm }}</h3>
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

<v-carousel-item>

<v-row align="center" dense>
    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/gimu.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[7].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/ipd.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[8].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/jantung.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[9].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/jiwa.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[10].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/kedokteran anak.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[11].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/mata.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[12].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Mikrobiologi.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[13].Nama_ksm }}</h3>
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

<v-carousel-item>

<v-row align="center" dense>
    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/OBG.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[14].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/ortho.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[15].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Parasitologi.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[16].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/paru.jpeg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[17].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Patologi.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[18].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Radiologi.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[19].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Radioterapi.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[20].Nama_ksm }}</h3>
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

<v-carousel-item>

<v-row align="center" dense>
    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Rehab Medik.jpg"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[21].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/Saraf.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[22].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/jantung.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[23].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/jantung.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[24].Nama_ksm }}</h3>
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

    <v-col align="center">
        <v-card variant="tonal"
                width="230"
                height="1000"
                color="surface-variant"
                > 
            <v-img height="150" src="/public/logoksm/jantung.png"></v-img>
            
            <v-card-title align="center">
                <h3>{{ ksm.data[25].Nama_ksm }}</h3>
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

</template> -->

<script setup>

import { useNow, useDateFormat } from '@vueuse/core'    
const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    


const tampungksm = await useFetch ('https://satu.dev.rssa.id/items/daftar_ksm')
const ksm = tampungksm.data



</script>