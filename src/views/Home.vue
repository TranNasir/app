<template>
  <div class="wrapper">
    <Title msg="Weather app"/>
    <Formzipcode />
  </div>
</template>

<script>
import Title from '@/components/Title.vue'
import Formzipcode from '@/components/Formzipcode.vue'
//@ way absolute

export default {
  name: 'App',
  components: {
    Title,
    Formzipcode
  }
}
</script>


<style>
.wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 400px;
  margin: auto;
}
</style>

