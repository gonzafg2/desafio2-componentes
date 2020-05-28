<template>
  <div id="app">

    <div class="container py-5 mt-5">
      <form @submit.prevent="agregar" @reset="limpiar" class="py-5 text-center">
        <div class="form-group">
          <label class="display-4">Tareas</label>
          <input v-model="tarea" type="text" class="form-control w-50 mx-auto my-5" placeholder="Ingrese nueva tarea">
        </div>
        <button type="submit" class="btn btn-success px-5 mx-5">Añadir</button>
        <button type="reset" class="btn btn-warning px-5 mx-5">Limpiar</button>
      </form>
      <Form :data=this.tareas></Form>
    </div>
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
      tarea: "",
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
