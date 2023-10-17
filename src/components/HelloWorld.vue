<template>
  <div class="hello">
    <button @click="handleClick(0)">关于</button>
    <button @click="handleClick(1)">详情</button>
    <button @click="handleClick(2)">主页</button>
    <component v-bind:is="list[idx]"></component>
  </div>
</template>

<script>
import {defineAsyncComponent } from 'vue';
const AboutDemo=defineAsyncComponent({ loader:()=>import('./AboutDemo.vue'),})
const DetailDemo=defineAsyncComponent({ loader:()=>import('./DetailDemo'),})
const HomeDemo=defineAsyncComponent({loader:()=>import('./HomeDemo.vue')})
export default {
  name: 'HelloWorld',
  components:{
    AboutDemo,
    DetailDemo,
    HomeDemo
  },
  data(){
    return{
      idx:1,
      list:['AboutDemo','DetailDemo','HomeDemo']
    }
  },
  methods:{
   handleClick(idx){
    console.log(idx)
    this.idx=idx;
   }
    }
  }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
