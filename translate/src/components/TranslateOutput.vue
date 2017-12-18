<template>
  <div id="translateOutput">
    <h2 id="output">{{translatedText}}</h2>
  </div>
</template>

<script>
export default {
  name: 'translateOutput',
  props: ['translatedText']
}
</script>

<style>
  #output{
    color: #ff9900;
  }
</style>
