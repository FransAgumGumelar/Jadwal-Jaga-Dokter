<template>
    <v-app-bar class="bg-red">
        <div class="center">
            <div class="text-h2 "> 
            {{ now }}
        </div>
        </div>
        
        <v-spacer />

        
    </v-app-bar>

</template>

<script setup lang="ts">
    import { useNow, useDateFormat } from '@vueuse/core'
    
    const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    

</script>