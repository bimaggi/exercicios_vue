<template>
    <div class="vif">
        <h1>Aula 9 v-if </h1>
        <a href="#init">Voltar pro inicio</a>

        <!--Não podemos usar o v-if na mesma tag que o v-for, 
            por isso vamos transforar a tag li em uma tag template ficticia e 
            dentro dessa template criar a tag li -->
        <div>
            <ul>
              <template v-for="num of 10" :key="num">
                  <li v-if="num%2 == 0" :key="num">
                      {{num}}
                  </li>
              </template>
            </ul>
        </div>
        
        <div>
            <ul v-if=" list.length > 1">
                <template v-for="item of list">
                    <li v-if="item % 2 === 0" :key="item">
                        {{item}}
                    </li>
                </template>
            </ul>
            <h2 v-else-if="list.length === 1">
                O único item da lista é:{{list[0]}}
            </h2>
            <h2 v-else>
                A lista está vazia
            </h2>
        </div>
    </div>

</template>
<script>
export default {
    name:'VifVue',
    data(){
        return{
            list:[10],
        }
    }
}
</script>

<style scoped>
.vif{
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
