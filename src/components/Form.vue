<template>
  <div class="form container text-center">
    
    <h3>Listado de Tareas</h3>
    <section class="tareas d-flex flex-row justify-content-center mt-4">
      <ul>
        <li v-for="item in data" :key="item.id" class="py-2">
          {{ item }} <button class="btn btn-danger btn-sm ml-3">Eliminar</button>
        </li>
        
      </ul>
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
    eliminarTarea() {

    }
  }
};
</script>

<style scoped lang="scss"></style>
