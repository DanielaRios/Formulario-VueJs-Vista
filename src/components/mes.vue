<script setup>
const meses = [
    'Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio',
    'Julio', 'Agosto', 'Septiembre', 'Octubre', 'Noviembre', 'Diciembre'
];
</script>
<template>
    <select id="mes" name="mes">
        <option value="" disabled selected>Mes</option>
        <option v-for="mes in meses" :value="mes" :key=mes> 
            {{ mes }}
        </option>
    </select>
</template>