<template>
    <select id="dia" name="dia">
        <option value="" disabled selected>Día</option>
        <option v-for="dia in 31" :value =dia :key = dia> {{ dia }} </option>
    </select>
</template>
