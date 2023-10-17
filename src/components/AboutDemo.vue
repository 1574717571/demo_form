<template>
    <div>
        <button @click="handleClick">about</button>
    </div>
</template>
<script>
export default {
  name: 'AboutDemo',
  data(){
    return{
      message:"about",
      show:false
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

</style>