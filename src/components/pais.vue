<script setup>
const paises = [
    'Argentina', 'Bolivia', 'Brasil', 'Chile', 'Colombia', 'Costa Rica',
    'Cuba', 'Ecuador', 'El Salvador', 'España', 'Estados Unidos', 'Guatemala',
    'Honduras', 'México', 'Nicaragua', 'Panamá', 'Paraguay', 'Perú',
    'Puerto Rico', 'República Dominicana', 'Uruguay', 'Venezuela'
];
</script>

<template>
    <select id="pais" name="pais">
        <option value="" disabled selected>Pais</option>
        <option v-for="pais in paises" :value="pais" :key="pais">
            {{ pais }} 
        </option>
    </select>

</template>