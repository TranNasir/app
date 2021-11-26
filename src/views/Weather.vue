<template>
  <div class="wrapper">
    <Title msg="Weather page"/>
    <weatherShow />
  </div>
</template>

<script>
import Title from '@/components/Title.vue'
import weatherShow from '@/components/Weathershow.vue'


export default {
  name: 'Weather',
  components: {
    Title,
    weatherShow
  }
}
</script>


<style>

</style>
