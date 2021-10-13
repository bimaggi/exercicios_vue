<template>
    <div class="links">
      <div><a rel="stylesheet" href="#data">Aula 5 - Data</a></div>
      <div><a rel="stylesheet" href="#event">Aula 6 - Event</a></div>
      <div><a rel="stylesheet" href="#bind">Aula 7 - Bind</a></div>
      <div><a rel="stylesheet" href="#vfor">Aula 8 - v-for</a></div>
      <div><a rel="stylesheet" href="#vif">Aula 9 - v-if</a></div>
      <div><a rel="stylesheet" href="#functions">Aula 10 - Funções</a></div>
      <div><a rel="stylesheet" href="#hooks">Aula 13 - Hooks</a></div>
    </div>
</template>

<script>
export default {
    name: 'HeaderVue',
}
</script>
<style scoped>
.links{
  display: flex;
  justify-content: space-between;
  margin: 15px;  
  margin-top: 50px;
  margin-bottom: 50px;

}
a{
  text-decoration: none;
  color: white;
  border: 1px solid white;
  padding: 8px;
}


</style>