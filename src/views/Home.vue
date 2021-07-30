<template>
  <form @submit.prevent="procesarFormulario">
    <input 
      type="text"
      class="form-control my-2"
      placeholder="Ingrese nombre"
      v-model.trim="tarea.nombre"
    >
    <div class="form-check form-check-inline">
      <input type="checkbox" id="check-1" class="form-check-input" v-model="tarea.categorias" value="Javascript">
      <label for="check-1" class="form-check-label">Javascript</label>
    </div>
    <div class="form-check form-check-inline">
      <input type="checkbox" id="check-2" class="form-check-input" v-model="tarea.categorias" value="Python">
      <label for="check-2" class="form-check-label">Python</label>
    </div>
    <div class="form-check form-check-inline">
      <input type="checkbox" id="check-3" class="form-check-input" v-model="tarea.categorias" value="Node JS">
      <label for="check-3" class="form-check-label">Node JS</label>
    </div>
    <div class="form-check form-check-inline">
      <input type="checkbox" id="check-4" class="form-check-input" v-model="tarea.categorias" value="Ruby">
      <label for="check-4" class="form-check-label">Ruby</label>
    </div>
    <div class="mt-2">
      <div class="form-check form-check-inline">
        <input type="radio" id="radio-1" class="form-check-input" v-model="tarea.estado" value="Urgente">
        <label for="radio-1" class="form-check-label">Urgente</label>
      </div>
      <div class="form-check form-check-inline">
        <input type="radio" id="radio-2" class="form-check-input" v-model="tarea.estado" value="Realax">
        <label for="radio-2" class="form-check-label">Relax</label>
      </div>
    </div>
    <div class="mt-2">
      <input type="number" class="form-control" v-model.number="tarea.numero">
    </div>
    
    <button class="btn btn-dark mt-2 btn-block" type="submit">Procesar</button>
  </form>
  <p>
    {{ tarea }}
  </p>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  data() {
    return {
      tarea: {
        nombre: '',
        categorias: [],
        estado: '',
        numero: 0
      }
    }
  },
  methods: {
    procesarFormulario(){
      console.log(this.tarea)
    }
  }
}
</script>
