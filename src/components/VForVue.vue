<template>
<div class="vfor">
    <h1>Aula 8 v-for</h1>
        <a href="#init">Voltar pro inicio</a>
    <!--o item e o index, podem ser trocados por qualquer nome que terão o mesmo valor e a 
        mesma posição-->
    <ul>
        <li v-for="(item,index) of fruitList" :key="index">
            {{item}}
        </li>
    </ul>
    <!-- Posso usar tanto o in qto o of no v-for , mas por semantica qdo for obj, usamos in
        o value e o property, podem ser trocados por qualquer nome que terão o mesmo valor e a 
        mesma ordem
        -->
    <ul>
        <li v-for="(value,property) in foodList" :key="property">
            {{property}} - {{value}}
        </li>
    </ul>
    <h4>Agora vamos adicionar mais uma fruta à lista</h4>
    <button @click="fruitList.push('açaí')">Adicionar fruta</button>
</div>
</template>

<script>
export default {
    name:'VForVue',
    data(){
        return {
            fruitList:[
                'morango',
                'amora', 
                'cereja',
                'framboesa'
            ],
            foodList:{
                carne:'filé de frango',
                salada:'Rúcula',
                bebida:'Suco de laranja'
            },
        }
    }
}
</script>
<style scoped>
.vfor{
  max-width: 70%;
  background: white;
  color: purple;
  border-radius: 5px;
  padding: 10px;
  margin: auto;
  margin-top:40px ;
  text-align: center;
}
a{
    color: purple;
}
li{
    list-style: none;
}

</style>
