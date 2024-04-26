<template>
    <div class="bg-red text-center">
            {{ now }}
        </div>
        
    <v-carousel
            height="560"
            show-arrows="hover"
            cycle
            hide-delimiter-background
            :interval="5000"
    >
        
        <v-carousel-item
            class="bg-light-green-accent-2 text-center"
            >
            sfsd
            
                
                <v-row >

                    <v-col cols="12" md="4">
                        <v-card
                            subtitle="This is a card subtitle"
                            text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!"
                            title="This is a title"
                        >
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4" >
                        <v-card >
                            <template v-slot:title>
                            KSM 1
                            </template>
                            <template v-slot:subtitle>
                            This is a card subtitle
                            </template>
                            <template v-slot:text >
                            Jaga 1:
                            <br> 
                            Jaga 2:
                            <br> 
                            Jaga Chif:
                            <br>
                            SPV:
                            <br>
                            </template>
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4" >
                        <v-card>
                            <v-card-item>
                            <v-card-title>KSM 3</v-card-title>
                            <v-card-subtitle>This is a card subtitle</v-card-subtitle>
                            </v-card-item>
                            <v-card-text>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!
                            </v-card-text>
                        </v-card>
                    </v-col>

                </v-row>

                <v-row>
                    
                    <v-col cols="12" md="4">
                        <v-card
                            title="This is a title"
                            subtitle="This is a card subtitle"
                            text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!"
                        >
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-card>
                            <template v-slot:title>
                            This is a title
                            </template>
                            <template v-slot:subtitle>
                            This is a card subtitle
                            </template>
                            <template v-slot:text>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!
                            </template>
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-card>
                            <v-card-item>
                            <v-card-title>This is a title</v-card-title>
                            <v-card-subtitle>This is a card subtitle</v-card-subtitle>
                            </v-card-item>
                            <v-card-text>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!
                            </v-card-text>
                        </v-card>
                    </v-col>

                </v-row>

                <v-row>
                    
                    <v-col cols="12" md="4">
                        <v-card
                            subtitle="This is a card subtitle"
                            text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!"
                            title="This is a title"
                        >
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-card>
                            <template v-slot:title>
                            This is a title
                            </template>
                            <template v-slot:subtitle>
                            This is a card subtitle
                            </template>
                            <template v-slot:text>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!
                            </template>
                        </v-card>
                    </v-col>

                    <v-col cols="12" md="4">
                        <v-card>
                            <v-card-item>
                            <v-card-title>This is a title</v-card-title>
                            <v-card-subtitle>This is a card subtitle</v-card-subtitle>
                            </v-card-item>
                            <v-card-text>
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus!
                            </v-card-text>
                        </v-card>
                    </v-col>

                </v-row>

                
                
        </v-carousel-item>

            <v-carousel-item
                src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
                cover
            >
        </v-carousel-item>

            <v-carousel-item
                src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                cover
            >
            </v-carousel-item>
        </v-carousel>

    
    
    
    </template>
    
    <script setup>
    
    import { useNow, useDateFormat } from '@vueuse/core'
    
    const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    

    </script>






