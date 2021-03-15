<template>
 <div class="container">

  <div class="rightbox">
    <div class="rb-container">
      <ul class="rb">
        <li class="rb-item" v-for="(item,i) in invertir_fechas" :key="i">
          <div class="timestamp">
            {{ item.fecha }}
          </div>
          <div class="item-title">{{ item.extracto }}</div>
        </li>
      </ul>

    </div>
  </div>
</div>
</template>

<script>

export default {
  name: 'TimeLine',
  data () {
    return{
      historial : [
        { fecha : '13 feb', extracto : 'En agradecimiento a trabajar en pandemia. JUST indica que descansemos todo el feriado de Carnaval. Es el inicio de la estafa programada.'},
        { fecha : '16 feb', extracto : 'Reunión por Zoom convocada por JUST. Informan que nuestras tareas habían sido llevadas a Escobar quedando a cargo de la empresa TRANSFARMACO (60 km de distancia).Solicitan desvinculación de JUST más Indemnización a su criterio y comodidad por oportunidad de entrevista en TRF. Es una clara extorsión'},
        { fecha : '16 feb', extracto : 'Los trabajadores en asamblea decidimos defender nuestras fuentes de trabajo.La trampa del feriado de carnaval se había ejecutado.'},
        { fecha : '17 feb', extracto : 'Constatamos con tristeza que la empresa estaba vacía. Se presenta el apoderado de la compañía ofrece reuniones individuales.'},
        { fecha : '23 feb', extracto : 'El Ministerio de Trabajo de La Plata decretó conciliación obligatoria ha solicitud del sindicato de comercio zona oeste (SEOCA) sin consulta previa'},
        { fecha : '26 feb', extracto : 'JUST simula acatar conciliación obligatoria. Sin embargo, intenta cambiar nuestro horario habitual .Tampoco trae actividades para realizar. Fraude total'},
        { fecha : '1 mar', extracto : 'Decidimos nuestra salida de SEOCA por desacuerdos en la forma de encarar el conflicto. Sindicato CIS (CTA autónoma) adhiere a nuestra causa. Denunciamos a JUST por vaciamiento, lockout patronal. Etc.'},
        { fecha : '4 mar', extracto : 'Realizamos caravana de autos por medios masivos denunciando nuestra situación.  Resultados muy positivos'},
        { fecha : '8 mar', extracto : 'Se coordina en Argentina (sindicato CTA Autónoma, partidos, movimientos sociales) y Suiza (sindicato UNIA) reclamos en las plantas Just de ambos países.'},
        { fecha : '10 mar',extracto : 'Realizamos una movilización junto a las organizaciones sociales, partidos políticos, y el sindicato CIS. Dicha acción se combino con el sindicato UNIA de Suiza que se presento en la planta ubicada en la ciudad de Walsenhausen haciendo suyo nuestro reclamo.'}
      ]
    }
  },
  computed:{
    invertir_fechas(){
      return this.historial.slice().reverse()
    }
  }
}
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=PT+Sans&display=swap");

body {
  background: #e8cbc0;
}

.container {
  background: #232931;
  width: 100%;
  margin: 0 auto;
  position: relative;
  box-shadow: 2px 5px 20px rgba(119, 119, 119, 0.5);
  font-size: 2.5rem;
}

.leftbox {
  top: -5%;
  left: 5%;
  position: absolute;
  width: 15%;
  height: 110%;
  background-color: #50d890;
  box-shadow: 3px 3px 15px rgba(119, 119, 119, 0.5);
}


.rightbox {
  padding: 0em 34rem 0em 0em;
  height: 100%;
}

.rb-container {
  font-family: "PT Sans", sans-serif;
  width: 50%;
  margin: auto;
  display: block;
  position: relative;
}

.rb-container ul.rb {
  margin: 2.5em 0;
  padding: 0;
  display: inline-block;
}

.rb-container ul.rb li {
  list-style: none;
  margin: auto;
  margin-left: 1.1em;
  min-height: 50px;
  border-left: 1px dashed #fff;
  padding: 0 0 50px 30px;
  position: relative;
}

.rb-container ul.rb li:last-child {
  border-left: 0;
}

.rb-container ul.rb li::before {
  position: absolute;
  left: -18px;
  top: 2px;
  content: " ";
  border: 8px solid rgba(255, 255, 255, 1);
  border-radius: 500%;
  background: #50d890;
  height: 20px;
  width: 20px;
  transition: all 500ms ease-in-out;
}

.rb-container ul.rb li:hover::before {
  border-color: #232931;
  transition: all 1000ms ease-in-out;
}

ul.rb li .timestamp {
  color: #50d890;
  position: relative;
  width: 600px;
  font-size: 30px;
}

.item-title {
  color: #fff;
}

.container-3 {
  width: 5em;
  vertical-align: right;
  white-space: nowrap;
  position: absolute;
}


</style>
