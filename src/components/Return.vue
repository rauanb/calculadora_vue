<script setup>
    const props = defineProps([
        'mostraOperador1',
        'mostraOperador2',
        'mostraOperacao',
        'mostraResposta'
        ]);
</script>

<template>
    <!-- <span>{{ props.mostraResposta }}</span> -->
    <span>{{ mostraOperador1 }} {{ props.mostraOperacao }} {{ mostraOperador2 }} = {{ mostraResposta }}</span>
</template>

<style scoped>

</style>