<template>
  <div class="form container">
    
    <section class="tareas">
      <ul>
        <li v-for="item in data" :key="item.id">
          {{ item }}
        </li>
        <button class="btn btn-danger btn-md">Eliminar</button>
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
