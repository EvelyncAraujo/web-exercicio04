<script setup>
import{ ref } from 'vue' 
  const contador = ref(0)
  let v1 = ref(0);  
  let v2 = ref(0);


  function soma() {
      return `A soma  é ${(v2.value * 1) + (v1.value)*1}`
    }
    function par(){
      if (soma() % 2 === 0){
        return `A soma é par`
      }
      }
    
</script>

<template>
     <div class="info">
      contador:{{ contador }}
      <button @click="contador++">+</button>
      <button @click="contador--">-</button>
      <div v-if="contador> 10" class="verde">É maior que 10</div>
      <div v-else-if="contador <10" class="vermelho">É menor que 10</div>
      <div v-else class="amarelo">É 10 </div>
 </div>

<div class="soma">
  <P class="texto">
      Informe dois números (Obs: tire os zeros)
    </P>

        <input v-model="v1">
        <input v-model="v2">
        <p>{{ soma() }}</p>
        
    <div v-if="v1+v2> 10" class="verde">É maior que 10</div>
    <div v-else-if=" v1+v2 < 10" class="vermelho">É menor que 10</div>
</div>

<div class="parImpar">
  <P class="texto">
      Informe dois números (Obs: tire os zeros)
    </P>

        <input v-model="v1">
        <input v-model="v2">
        <p>{{ par() }}</p>
        <div v-if="v1 & v2 <= par" class="verde">É Par</div>
      <div v-else class="vermelho">É Ímpar</div>
</div>

<div class="booleano">


</div>
</template>



<style scoped>
.booleano{
  background-color: rgb(105, 53, 53);
  padding: 50px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin: 40px 20px;
}

.parImpar{
  background-color: rgb(105, 53, 53);
  padding: 50px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin: 40px 20px;
}
.soma{
  background-color: rgb(105, 53, 53);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin: 0 20px;
}
.info {
  background-color: rgb(105, 53, 53);
  padding: 10px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
  margin: 0 20px;
}
h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
.verde{
    color: rgb(12, 58, 12);
}
.vermelho{
    color: rgb(71, 8, 8);
}
.amarelo{
    color: rgb(187, 187, 0);
}
</style>