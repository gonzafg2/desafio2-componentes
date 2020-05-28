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
      <Form @tareaEliminada="tareaAEliminar" :data=this.tareas></Form>
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
      tareas: ["Pagar Internet", "Comprar Pan", "Pagar Netflix"],
      tareaId: null
    }
  },
  methods: {
    agregar() {
      try {
        if (this.tarea !== "") {
          this.tareas.push(this.tarea)
        }
      } catch (error) {
        console.log(error)
      } finally {
        this.tarea = ""
      }
    },
    limpiar() {
      this.tarea = ""
    },
    tareaAEliminar(id) {
      this.tareaId = id
      
      try {
        this.tareas.splice(id, 1)
      } catch (error) {
        console.log(error)
      } finally {
        this.tareaId = ""
      }
    }
  }
};
</script>

<style lang="scss"></style>
