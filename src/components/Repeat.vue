<template>
<div>
 <span v-for="r in repetitions" :key="r">
   {{content}}
  </span>
</div>
</template>

<script>
export default {
  props: ['time','content'],
  computed:{
    repetitions(){
      return Array.from({length:this.time},(v,k)=>k+1)
    }
  }
}
</script>

<style scoped>

</style>