<template>
<div>
 <span v-for="r in repetitions" :key="r">
   {{content}}
  </span>
</div>
</template>

<script>
export default {
  name: "Repeat"
}
</script>

<style scoped>

</style>