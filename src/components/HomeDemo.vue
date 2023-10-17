<template>
    <div>
        <button @click="handleClick">hello world vue!</button>
        <Transition name="fade">
            <h1 v-if="show">Vue</h1>
        </Transition>
    </div>
</template>
<script>
export default {
  name: 'HomeDemo',
  data(){
    return{
      message:"你好",
      show:true
    }
  },
  methods:{
    handleClick(){
      this.show=!this.show
    }
  }
}
</script>
<style>
.fade-enter-active, .fade-leave-active{
    transition:opacity 5s;
}
.fade-enter, .fade-leave-to{
    opacity: 0;
}
</style>