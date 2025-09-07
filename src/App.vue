<script setup>
import Dia from './components/dia.vue'
import Mes from './components/mes.vue'
import Anio from './components/anio.vue'
import LabelInput from './components/labelInput.vue';
import Pais from './components/pais.vue';
import Ofertas from './components/ofertas.vue';

const imprimirFormulario = (e) =>{
  e.preventDefault(); // evitar recargar la pagina
  const formulario = new FormData(e.target); // crea un objeto FormData con los datos del formulario
  // Recorre los datos del formulario e imprime cada par clave-valor
  formulario.forEach((value, key) => {
    console.log(key + ": " + value);
  });
}
</script>

<template>
  <form @submit="imprimirFormulario">
    <header>
      <h1>RELIA</h1>
      <h2>Formulario de registro</h2>
    </header>
    <hr class="separador">
    </hr>


    <fieldset class="contenedor-datos">
      <legend>¿Quien sos?</legend>
      <LabelInput titulo="Nombre" id="fnombre" />
      <LabelInput titulo="Apellido" id="fapellido" />
      <LabelInput titulo="Correo Electronico" id="fcorreo" />
      <div class="item">
        <label for="fnacimiento">Fecha Nacimiento</label>
        <div class="fecha-nacimiento">
          <Dia />
          <Mes />
          <Anio />
        </div>
      </div>
    </fieldset>

    <fieldset class="contenedor-datos">
      <legend>¿De donde sos?</legend>
      <LabelInput titulo="Ciudad" id="fciudad" />
      <LabelInput titulo="Codigo Postal" id="fpostal" />
      <div class="item">
        <label for="fpais">País</label>
        <div class="fecha-nacimiento">
          <Pais />
        </div>
      </div>
    </fieldset>
    <fieldset class="contenedor-datos">
      <legend>¿Como queres iniciar sesion?</legend>
      <LabelInput titulo="Nombre de usuario" id="fusuario" />
      <LabelInput titulo="Contraseña" id="fcontraseña" tipo="password" />
      <LabelInput titulo="Repetir Contraseña" id="frepetir" tipo="password" />
    </fieldset>
    <fieldset class="contenedor-datos">
      <legend>Condiciones de registro</legend>
      <p>Deseo recibir ofertas de Relia</p>
      <div class="radio">
        <Ofertas titulo="Una vez al dia" id="undia" nombre="oferta" />
        <Ofertas titulo="Una vez por semanas" id="unasemana" nombre="oferta" />
        <Ofertas titulo="Una vez por mes" id="unames" nombre="oferta" />
      </div>
      <div class="radio">
        <input type="checkbox" id="terminos" name="terminos" value="terminos"></input>
        <label for="terminos">Acepto el acuerdo de servicios, la declaracion de privacidad y la declaracion de
          cookies.</label>
      </div>
    </fieldset>
    <div class="contenedor-boton">
      <button type="submit" class="boton">Crear cuenta</button>
    </div>
  </form>
</template>

<style scoped>
.fecha-nacimiento {
  display: flex;
  gap: 20px;
}

.contenedor-datos {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-bottom: 20px;
  padding-bottom: 20px;
}

.item {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.separador {
  margin-bottom: 10px;
}

.radio {
  display: flex;
  flex-direction: row;
  gap: 10px;
}

.contenedor-boton {
  display: flex;
  justify-content: center;
  /* centra horizontalmente */
  margin-top: 20px;
  /* espacio arriba */

}

.boton {
  font-size: 20px;
  /* texto más grande */
  padding: 10px 30px;
  /* agranda el botón */
  font-weight: bold;
  /* texto en negrita */
}

legend {
  font-weight: bold;
}

header {
  text-align: center;
  margin-bottom: 10px;
}
</style>
