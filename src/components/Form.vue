<template>
  <div class="form container text-center">
    
    <h3>Listado de Tareas</h3>
    <section class="tareas d-flex flex-row justify-content-center mt-4">
      <ol>
        <li v-for="(item, index) in data" :key="index" class="py-2 items">
          {{ item }} <button @click="eliminarTarea(index)" class="btn btn-danger btn-sm ml-3">Eliminar</button>
        </li>
        
      </ol>
    </section>
  </div>
</template>

<script>
export default {
  name: "Form",
  props: {
    data: {
      type: Array
    }
  },
  data() {
    return {
      
    }
  },
  methods: {
    eliminarTarea(id) {
      this.$emit("tareaEliminada", id);
    }
  }
};
</script>

<style scoped lang="scss">
.items{
  font-size: 1.25rem;
  font-weight: 500;
}
</style>
