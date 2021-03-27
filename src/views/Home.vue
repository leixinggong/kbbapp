<template>
  <div class="home">
    <glButton>
      <div>O-O</div>
    </glButton>
    <svg-icon icon="wechat"></svg-icon>
  </div>
</template>

<script>
import glButton from '../componets/gl-button'

export default {
  name: 'Home',
  components: {
    glButton
  }
}
</script>

<style scoped>

  .container {
    background-color: red;
  }
</style>
