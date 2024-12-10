<script setup>
    const props = defineProps([
        'alteraOperacao',
        'alteraOperador1',
        'alteraOperador2'
        ])
</script>

<template>
    <form>
        <div class="row">
            <div class="col">
                <input
                @change="alteraOperador1"
                class="form-control"
                type="number"
                placeholder="Número 1">
            </div>
            <div class="col">
                <input
                @change="alteraOperador2"
                class="form-control"
                type="number"
                placeholder="Número 2">
            </div>
            <div @change="props.alteraOperacao" class="col">
                <select class="form-control">
                    <option value="Soma">Soma</option>
                    <option value="Subtracao">Subtração</option>
                    <option value="Multiplicacao">Multiplicação</option>
                    <option value="Divisao">Divisão</option>
                </select>
            </div>
        </div>
    </form>
</template>

<style scoped>
    /* p {
        background-color: aqua;
    } */
</style>