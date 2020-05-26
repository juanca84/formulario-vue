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
          <div class="form-group">
            <label for="email">Email:</label>
            <input type="text" id="email" class="form-control" v-model='datosPersona.email'>
          </div>
          <div class="form-group">
            <label for="mensaje">Mensaje:</label>
            <textarea name="mensaje" id="mensaje" cols="60" rows="10" class="form-control" v-model="mensaje"></textarea> 
          </div>
        </div>
      </div>
    </form>
    <div class="row">
      <div class="col-xs12 col-sm-8 col-md-6">
        <hr>
        <div class="panel panel-default">
          <div class="panel-heading">
            <h3 class="text-center">Datos Ingresados</h3>
          </div> 
          <div class="panel-body">
            <p><strong>Nombre:</strong> {{datosPersona.nombre}}</p>
            <p><strong>Email:</strong> {{datosPersona.email}}</p>
            <p><strong>Mensaje:</strong></p>
            <p class="formato-text-area">{{mensaje}}</p>
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
      },
      mensaje: 'Test mensaje'
    }
  }
}
</script>

<style scoped>
  .formato-text-area{
    white-space: pre;
  }
</style>
