<template>
  <div class="hello">
    <h1>{{testValue  }}</h1>
    <button @click="clickTest">修改</button>
  </div>
</template>

<script>
import { usestore } from '@/store/usestore';




export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
   return {
     testValue:'wqj'
   }
  },
  methods:{
    clickTest(){
      usestore.name="已经改变";
      this.testValue=usestore.name;
    }
  },
  mounted(){
    this.testValue=usestore.name;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
