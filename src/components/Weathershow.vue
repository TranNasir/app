<template>
  <div class="weathershow">
    <p>{{city}}</p>
  </div>
</template>

<script>

export default {
  name: 'weatherShow',

  data(){
    return {
      city: ''
    }
  },
  mounted() {
    this.city = localStorage.getItem('weatherZipcode');
  },
  methods: {
  }
}

</script>

<style >
.weathershow{
  width: 100%;
  max-width: 350px;
  height: 100%;
  min-height: 230px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin: auto;
  border: 1px solid #D3D3D3;
}
</style>