<template>
    <div class="bg-red text-center">
    {{ now }}
    </div>
</template>



<script setup lang="ts">
    
    import { useNow, useDateFormat } from '@vueuse/core'
    
    const now = useDateFormat(useNow(), "dddd, DD MMMM YYYY HH:mm:ss", {locales:'id-ID'})
    

</script>