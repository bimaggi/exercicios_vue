<template>
    <div class="bind">
        <h1>Aula7 v-bind</h1>
        <a href="#init">Voltar pro inicio</a>
        <h2>O v-bind é uma forma de deixar os atributos do html dinâmicos,conforme o dado é alterado</h2>
        <h3>Qual animal você prefere ?  </h3>
            <input 
                v-model="petImage"
                type="radio" 
                name="pet"
                id="cat" 
                value="https://ogimg.infoglobo.com.br/in/24649523-8a0-224/FT1086A/88249115.jpg"
                >
            <label for="cat">Gato</label>
            <input 
                v-model="petImage" 
                type="radio" 
                name="pet"
                id="dog" 
                value="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSRmD5YCmi5nZGVP2gUuodm3867dZu_2MX6SjHIz_md8UcUNQ9Aqxw9hiTMtMx2PmnWiP4&usqp=CAU"
                >
            <label for="dog">Cachorro</label>
            <div>
                <img v-bind:src="petImage" style="max-width:300px">
                 <!--<img :src="petImage" style="max-width:300px">-->
            </div>
            <div>
                <h1>Vamos desabilitar o botão quando atingir 5 elementos na lista</h1>
                <button :disabled="myList.length === 5" @click="myList.push('elemento')">Adicionar elemento</button>
                <div>{{myList}}</div>
            </div>
        </div> 
</template>

<script>
export default {
    name:'BindVue',
    data(){
        return{
            petImage:"",
            myList:[],
            newList:[],
        }
    }
}
</script>
<style scoped>
.bind{
  max-width: 70%;
  background: white;
  color: purple;
  border-radius: 5px;
  padding: 10px;
  margin: auto;
  margin-top:40px ;
  text-align: center;
}
</style>