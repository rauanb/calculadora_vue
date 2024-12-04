<template>
    <form>
        <div class="row">
            <div class="col">
                <input class="form-control" required type="number" placeholder="Número 1">
            </div>
            <div class="col">
                <input class="form-control" required type="number" placeholder="Número 2">
            </div>
            <div class="col">
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