<template>
    <div>
        <OBR></OBR>
        <Guide></Guide>
        <Tutorial></Tutorial>
    </div>
</template>

<script>
import OBR from '../components/OBR/index.vue';
import Guide from '../components/OBR/Guide.vue';
import Tutorial from '../components/OBR/Tutorial.vue';
export default {
    "name": "OBRPage",
    components: { OBR, Guide, Tutorial }
}
</script>

<style>
</style>