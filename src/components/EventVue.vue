<template>
<div class="dom">
    <h1>Aula 6 Evento Dom</h1>
    <a href="#init">Voltar pro inicio</a>
    <h1>Contador</h1>
    
    <div class="bodyDom">{{count}}</div>
    <div class="bodyDom">
        <button @click="count += 1"> + </button>
        <button @click="count -= 1"> - </button>
    </div>
    <div>
        <h1>Estado do input {{inputState}}</h1>
        <input type="text" placeholder="Clique aqui"
            @focus="inputState='Focado'"
            @blur="inputState='Saiu'"
        >
        <p>Clique aqui fora pra ver o estado do input</p>
    </div>
    <div>
        <form @submit.prevent="preventEvent='Evento Prevenido'">
            <h1>{{preventEvent}}</h1>
            <button>Clique aqui e veja se o evento foi prevenido</button>
        </form>
    </div>
</div>   
</template>

<script>
export default {
    name:'EventVue',
    data(){
        return{
            count:0,
            inputState:'',
            preventEvent:'Prevenir o evento submit',
        }
    }
}
</script>
<style scoped>
.dom{
  max-width: 70%;
  background: white;
  color: purple;
  border-radius: 5px;
  padding: 10px;
  margin: auto;
  margin-top:40px ;
  text-align: center;

}
.bodyDom{
    display: flex;
    justify-content: center;
}
p{
    color: red;
    font-style: italic;
    font-size: x-large;
}
a{
    color: purple;
   
}

</style>

