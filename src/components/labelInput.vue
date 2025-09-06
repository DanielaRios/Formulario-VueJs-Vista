<script setup>
const props = defineProps({
    titulo: String,
    id: String,
    tipo: {
        type: String,
        default: "text"
    }
});
</script>

<template>
<div class="item">    
<label :for=props.id>{{ props.titulo }}</label>
<input :type=props.tipo :id=props.id :name=props.id></input>
 </div>       
</template>

<style scoped>
.item {
  display: flex;
  flex-direction: column;
  gap: 2px;
}
</style>