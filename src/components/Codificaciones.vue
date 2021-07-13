<template>
  <section class="src-codificaciones">
      <div class="jumbotron">
        <h2>Exámen Final - Juan Ignacio Bartamian</h2>
        <br>
        <input type="text" v-model="texto">
        <hr>
        <h5> cantidad: {{ cantidadCaracteres}}</h5>
        <h5>{{ texto | replace("a","e")}} (codificado)</h5>
        <h5>{{ texto | mayus}} (Mayúscula)</h5>
        <h5>{{ texto | minus}} (Minúscula)</h5>
        <h5>{{ texto | mayusMinus}} (Mayúscula/Minúscula)</h5>
        <h5>{{ texto | minusMayus}} (Minúscula/Mayúscula)</h5>
      </div>
      <p>respuestas:1:b 2:b 3:c 4:b 5:b </p>
  </section>

</template>

<script lang="js">

  export default  {
    name: 'src-codificaciones',
    props: [],
    mounted () {

    },
    data () {
      return {
        texto: "",
      }
    },
    filters: {
      minusMayus: function(texto) {
        return texto.split('').map((char,index) => index % 2 == 0 ? char.toLowerCase() : char.toUpperCase()).join(''); 
      },
      mayusMinus: function(texto) {
        return texto.split('').map((char,index) => index % 2 == 0 ? char.toUpperCase() : char.toLowerCase()).join(''); 
      },
      mayus: function(texto) {
        return texto.toUpperCase();
      },
      minus: function(texto) {
        return texto.toLowerCase();
      },
      codificado: function(texto) {
        return texto.replace('o','e')
      },
      replace: function (texto) {
      const result = texto.toLowerCase().split("o").join("e").split("u").join("a");
      return result;
      }
    },
    methods: {
    },
    computed: {
      cantidadCaracteres(){
        return this.texto.length
      }
      

    }
}


</script>

<style scoped lang="css">
  .src-codificaciones {

  }

</style>
