<template>
  <div id="app">

    <form @submit.prevent="agregar" @reset="limpiar">
      <div class="form-group">
        <label>Tarea</label>
        <input v-model="tareas" type="text" /> type="text" class="form-control" placeholder="Ingrese nueva tarea">
      </div>
      <button type="submit" class="btn btn-success">Añadir</button>
      <button type="reset" class="btn btn-warning">Limpiar</button>
    </form>


    <Form :data=this.tareas></Form>
  </div>
</template>

<script>
import Form from "./components/Form.vue";

export default {
  name: "App",
  components: {
    Form
  },
  data() {
    return {
      tareas: []
    }
  },
  methods: {
    agregar() {

    },
    limpiar() {
      this.tarea = ""
    },
  }
};
</script>

<style lang="scss"></style>
