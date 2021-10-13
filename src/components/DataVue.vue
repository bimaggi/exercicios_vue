<template>
<div class="data">
  <div class="bodyData">
    <h1>Aula 5 Data</h1>
    <a href="#init">Voltar pro inicio</a>
    <h2>Olá meu nome é: {{nome}}</h2>
    <input type="text" v-model="nome" placeholder="Digite seu nome">
  </div>
  <div class="bodyData">
    <h3>Adiciona um número a cada 5 segundos => {{num}}</h3>
  </div>
</div>
</template>

<script>
export default {
  name:'DataVue',
  data(){
    return{
      nome:'',
      num:0,
      sec:0,
    }
  },
  mounted(){
    setInterval(()=>{
      this.num += 1
    },5000)
  }
  
}
</script>
<style scoped>
.data{
  max-width: 70%;
  background: white;
  color: purple;
  border-radius: 5px;
  padding: 10px;
  margin: auto;
  margin-top:40px ;

}
.bodyData{
  text-align: center;
}
h1{
  text-align: center;
}
a{
  color: purple;
}

</style>
