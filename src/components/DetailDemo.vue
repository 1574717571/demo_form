<template>
    <div>
        <button @click="handleClick">detail</button>
    </div>
</template>
<script>
export default {
  name: 'DetailDemo',
  data(){
    return{
      message:"detail parameter",
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