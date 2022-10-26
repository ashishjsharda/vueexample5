<template>
  <div>
    <h1>Hello {{who}}</h1>
  </div>
</template>
<script>
export default {
  name: 'Hello',
  props: {
    who: String
  }
}
</script>