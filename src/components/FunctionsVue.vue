<template>
    <div class="func">
        <h1>Aula 10 Functions - methods</h1>
        <a href="#init">Voltar pro inicio</a>

        <div>  
            <h1>Aqui os valores estão  definidos com : 3 + 2</h1>
            <button @click="somar(3,2)">somar</button>
            <div>Resultado:{{valor}}</div>
        </div>
        <div class="bodyFun">
            <h1>Aqui vamos pegar os valores dos inputs </h1>
            <input type="number" name="num1" id="num1" v-model="x" >
            <input type="number" name="num2" id="num2" v-model="y" >
            <button @click="soma(x,y)">Soma</button>
            <div>Total da soma:{{total}}</div>
        </div>


        <div class="bodyComp">
            <h1>Aula 11 Functions - computed</h1>
            <a href="#init">Voltar pro inicio</a>
            <p>
                Computed é um valor computado à partir de outros dados. A computed vai ser recalculada sempre 
                que o valor que estiver nela for alterado.
            </p>
            <input type="text" v-model="firstName" placeholder="digite seu orimeiro nome">
            <div>{{fullName}}</div>
             <h3>Vamos desabililtar o botão qdo tiver 5 elementos</h3>
            <div>{{list}}</div>
            <button :disabled="shouldDisabledButton" @click="addItem('elemento')">addElement</button>
        </div>
        <div class="bodyComp">
            <h1>Aula 12</h1>
            <a href="#init">Voltar pro inicio</a>

            <p>
                O watch vai ficar assistindo tanto o computed, como o data e qdo houver ateração neles
                o watch vai exectuar algum comando. O nome do metodo dentro do watch sempre vai ser o nome
                do dado que está sendo assistido
            </p>
            <h2>Aqui vamos ver alterações do watch: {{number}}</h2>
            <button @click="number= Math.floor(Math.random()*10)+1">Add watch</button>
        </div>
    </div>
   
</template>
<script>
export default {
        name:'FunctionsVue',
    data(){
        return{
            valor:0,
            total:0,
            x:0,
            y:0,
            firstName:'Marcia',
            lastName:'Oliveira',
            list:[1,2,3],
            number:0,
        }
    },
    methods:{
        somar(n1,n2){
            this.valor = n1+n2
        },
        soma(x,y){
            this.total = x+y
        },
        addItem(value){
            this.list.push(value)
        },
        isEven(){
            return this.number%2 === 0 
        }
    },
    computed:{
       fullName(){
           return `${this.firstName} ${this.lastName}`
       },
       shouldDisabledButton(){
           return this.list.length === 5
       }
    },
    watch:{
        number(value,oldValue){
            if(this.isEven(value)&& this.isEven(oldValue)){
                alert('Parabéns, já sairam 2 numeros pares')
            }
        }
    }
}
</script>
<style scoped>
.func{
  max-width: 70%;
  background: white;
  color: purple;
  border-radius: 5px;
  padding: 10px;
  margin: auto;
  margin-top:40px ;
  text-align: center;

}
.bodyFun{
    display: flex;
    max-width: 60%;
    flex-direction: column;
    justify-content: center;
    margin: auto;
}
.bodyFun input , .bodyFun button{
    max-width: 100%;
    padding: 3px;
    margin: 5px;
}
.bodyComp P{
    max-width: 80%;
    margin: auto;
    margin-top:30px;
    margin-bottom:30px;
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
