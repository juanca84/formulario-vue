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
          <div class="form-group">
            <input type="checkbox" id="enviaremail" value="enviaremail" v-model="opcionEmail">
            <label for="enviaremail" class="form-check form-check-inline">Enviar Email</label>
            <input type="checkbox" id="enviarcopia" value="enviarcopia" v-model="opcionEmail">   
            <label for="enviarcopia" class="form-check form-check-inline">Enviar Copia</label> 
          </div>
          <div class="form-group">
            <input type="radio" id="masculino" value="M" v-model="genero">
            <label for="masculino" class="form-check form-check-inline">Masculino</label>
            <input type="radio" id="femenino" value="F" v-model="genero">   
            <label for="femenino" class="form-check form-check-inline">Femenino</label> 
          </div>
          <div class="form-group">
            <label for="horario">Horario</label>
            <select id="horario" class="form-control" v-model="horario">
              <option v-for="item in datosHorario" :value="item" :key="item" :selected="horario=='Mañana'">{{item}}</option>
            </select>
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
            <p><strong>Opción de envío:</strong></p>
            <p>
              <ul>
                <li v-for="item in opcionEmail" :key="item">{{item}}</li>
              </ul>
            </p>
            <p><strong>Genero:</strong> {{genero}}</p>
            <p><strong>Horario:</strong> {{horario}}</p>
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
      mensaje: 'Test mensaje',
      opcionEmail: [],
      genero: 'M',
      datosHorario:['Mañana','Tarde','Noche'],
      horario: 'Mañana'
    }
  }
}
</script>

<style scoped>
  .formato-text-area{
    white-space: pre;
  }
</style>
