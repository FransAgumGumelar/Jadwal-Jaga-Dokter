<template>
    <H1>HALAMAN PPDS</H1>
    {{ datappds }}
</template>

<script setup lang="ts">

    const datappds = await useFetch('https://satu.dev.rssa.id/items/data_jadwal_jaga_dokter?filter[Jenis][_eq]=PPDS')
    

</script>