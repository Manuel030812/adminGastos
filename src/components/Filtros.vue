<template>
    <div class=" filtros sombra contenedor">

        <form>
            <div class="campo">
                <label for="filtro">Filtrar gastos</label>
                <select id="filtro" :value="filtro"
                    @input="$emit('update:filtro', $event.target.value)">
                    <option value="">--- Seleccione ---</option>
                    <option value="ahorro">Ahorro</option>
                    <option value="comida">Comida</option>
                    <option value="casa">Casa</option>
                    <option value="gastos">Gastos Varios</option>
                    <option value="ocio">Ocio</option>
                    <option value="salud">Salud</option>
                    <option value="suscripciones">Suscripciones</option>
                </select>
            </div>
        </form>

    </div>
</template>

<script setup>

defineProps(['filtro']);
defineEmits(['update:filtro']);

</script>

<style  scoped>
.filtros {
   margin-top: 10rem;

}
.filtros .campo{
    display: flex;
    align-items: center;
    gap: 2rem;

}
.filtros label{
    font-size: 3rem;
    font-weight: 900;
    color: var(--gris-oscuro);
}

.filtros select{
    flex : 1;
    padding: 1rem;
    border: none;
    border-radius: 1rem;
    background-color: var(--gris-claro);
    text-align: center;

}



</style>