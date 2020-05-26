<template>
  <div>
    <form>
      <div class="row">
        <div class="col-xs12 col-sm-8 col-md-6" >
          <h1 class="text-center">Formulario de Contacto</h1>
          <hr>
          <div class="form-group">
            <label for="nombre">Nombre:</label>
            <input type="text" id="nombre" class="form-control" v-model='datosPersona.nombre'>
          </div>
          <div clas="form-group">
            <label for="email">Email:</label>
            <input type="text" id="email" class="form-control" v-model='datosPersona.email'>
          </div>
        </div>
      </div>
    </form>
    <div class="row">
      <div class="col-xs12 col-sm-8 col-md-6">
        <hr>
        <div class="panel panel-default">
          <div class="panel-heading">
            <h3 class="text-center">Datos</h3>
          </div>
          <div class="panel-body">
            <p>Nombre: {{datosPersona.nombre}}</p>
            <p>Email: {{datosPersona.email}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Formulario',
  data(){
    return{
      datosPersona:{
        nombre:'',
        email:''
      }
    }
  }
}
</script>

<style scoped>
</style>
