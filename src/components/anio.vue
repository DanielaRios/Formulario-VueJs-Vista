<script setup>
const anios = [];
for (let i = 1960; i <= 2024; i++) {
    anios.push(i);
}
</script>

<template>
    <select id="anio" name="anio">
        <option value="" disabled selected>Año</option>
        <option v-for="anio in anios" :value="anio" :key="anio">
            {{ anio }}
        </option>
    </select>
</template>