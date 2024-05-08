<template>
  <div id="main" class="container row">
    <div id="formulario" class="col-sm-6">
      <div class="mb-3 row">
        <label for="inputTitle" class="col-sm-3 col-form-label">Título</label>
        <div class="col-sm-9">
          <input v-model="titulo" type="text" class="form-control" id="inputTitle">
        </div>
      </div>

      <hr/>
      
      <div class="mb-3 row">
        <label class="col-sm-3 col-form-label">Emogi</label>
        <div class="col-sm-9">
          <select v-model="emogi" class="form-select" aria-label="Default select example">
            <option disable value="">Seleccione un emogi</option>
            <option>📽</option>
            <option>👩‍💻</option>
            <option>🙅‍♂️</option>
            <option>📵</option>
          </select>
        </div>
      </div>

      <hr />

      <div class="mb-3 row">
        <label class="col-sm-3 col-form-label">Apreciación</label>
        <div class="col-sm-9">
          <input v-model="apreciacion" type="radio" name="apreciacion" value="Regular" id="inputRegular">
          <label class="col-form-label me-2" for="inputRegular">Regular</label>

          <input v-model="apreciacion" type="radio" name="apreciacion" value="Bien" id="inputBien">
          <label class="col-form-label me-2" for="inputBien">Bien</label>

          <input v-model="apreciacion" type="radio" name="apreciacion" value="Muy bien" id="inputMuyBien">
          <label class="col-form-label me-2" for="inputMuyBien">Muy bien</label>

          <input v-model="apreciacion" type="radio" name="apreciacion" value="Increible" id="inputIncreible">
          <label class="col-form-label me-2" for="inputIncreible">Increible</label>
        </div>
      </div>

      <hr/>

      <div class="mb-3 row">
        <label class="col-sm-3 col-form-label">Competencias aprendidas</label>
        <div class="col-sm-5">
          <input v-model="competencias" type="checkbox" name="morfologia" value="Morgología de un componente" id="morfologia">
          <label class="col-form-label" for="morfologia">Morfología de un <br/> componente</label>
          <br/>
          <input v-model="competencias" type="checkbox" name="one-way" value="One-Way & Two-Way data binding" id="one-way">
          <label class="col-form-label" for="one-way">One-Way & Two-Way <br/> data binding</label>
          <br/>
          <input v-model="competencias" type="checkbox" name="patron" value="El patroón de diseño MVC" id="patron">
          <label class="col-form-label" for="patron">El patroón de diseño <br/> MVC</label>
        </div>
        <div class="col-sm-4">
          <input v-model="competencias" type="checkbox" name="directivas" value="Directivas" id="directivas">
          <label class="col-form-label" for="directivas">Directivas</label>
          <br/>
          <input v-model="competencias" type="checkbox" name="estado" value="Estado" id="estado">
          <label class="col-form-label" for="estado">Estado</label>
        </div>
      </div>

      <hr/>

      <div class="form-floating">
        <textarea v-model="opinion" class="form-control" style="height: 60px"></textarea>
        <label for="floatingTextarea2">Opinión</label>
      </div>
    </div>

    <div class="col-sm-6" id="componenteVisual">
      <h1>{{ emogi }}</h1>
      <h2>{{titulo}}</h2>
      <p>El curso me ha parecido: {{ apreciacion }} </p>
      <p>He aprendido: {{ competencias }}</p>
      <p>Mi opinión hasta ahora es: {{ opinion }}</p>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'App',
  data(){
    return {
      titulo: "",
      emogi: "",
      apreciacion: "",
      competencias: ref([]),
      opinion: ""
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
