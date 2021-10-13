<template>
    <div id="init">
      <h1>Fundamentos do Vue</h1>
      <header-vue />
      <data-vue id="data"/>
      <event-vue id="event"/>
      <bind-vue id="bind"/>
      <vfor-vue id="vfor"/>
      <vif-vue id="vif"/>
      <functions-vue id="functions"/>
      <hooks-vue id="hooks"/>
    </div>
</template>
i
<script>
import EventVue from '@/components/EventVue'
import DataVue from '@/components/DataVue'
import BindVue from '@/components/BindVue'
import VforVue from '@/components/VForVue' 
import VifVue from '@/components/VifVue'
import FunctionsVue from '@/components/FunctionsVue'
import HooksVue from '@/components/HooksVue'
import HeaderVue from '@/components/HeaderVue'

export default {
  name:'App',
  components:{
    DataVue,
    EventVue,
    BindVue,
    VforVue,
    VifVue,
    FunctionsVue,
    HooksVue,
    HeaderVue,
  }
}
</script>
<style>
body{
  background: rgb(107, 66, 107);
  color: white;
}
h1{
  text-align: center;
  margin-top: 50px;
  margin-bottom: 0;
}
</style>