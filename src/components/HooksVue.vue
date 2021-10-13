<template>
<div class="hooks">
    <h1>Aula 13 - lyfeCicle Hooks</h1>
    <a href="#init">Voltar pro inicio</a>
    <h2>vai adicionar 1 numero a mais a cada 2 segundos {{num}}</h2>
</div>
</template>
<script>
export default {
    name:'HooksVue',
    data(){
        return{
            num:0
        }
    },
    beforeCreate(){
        console.log('beforeCreate')
    },
    created(){
        console.log('created')

    },
    beforeMount(){
        console.log('beforeMount')

    },
    mounted(){
        console.log('mounted')
        setInterval(()=>{
            this.num += 1
        },2000)

    },
    updated(){
        console.log('updated')

    },
    beforeUnmount(){
        console.log('beforeDestroy')
        // alert('vai destruir')
    }
}
</script>

<style scoped>
.hooks{
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

</style>
