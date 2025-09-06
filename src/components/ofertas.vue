<script setup>
const props = defineProps({
    titulo: String,
    id: String,
    nombre: String
})

</script>

<template>
<div class="alineado">
    <input type="radio" :id=props.id :name=props.nombre :value=props.id></input>
    <label :for=props.id>{{ props.titulo }}</label>
</div>
</template>

<style scoped>
.alineado {
  display: flex;
  align-items: center; /* alinea verticalmente */
  gap: 8px;            /* espacio entre radio y texto */
  margin-bottom: 10px;  /* separación entre opciones */
}
</style>