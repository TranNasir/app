<template>
  <div class="weatherForm">
    <form 
      class="form-weather">
      <div class="zipcode-content">
        <input 
          type="text"
          v-model="zipcode" 
          placeholder="Veuillez entrer votre code postal :"
          required
        />
      </div>
      <div class="zipcode-submit">
        <input type="submit" placeholder="Soumettre" @click="setCity">
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'formZipcode',
  props: {
    msg: String
  },
  data(){
    return {
      zipcode: '',
    }
  },
  mounted() {
    this.zipcode = localStorage.getItem('weatherZipcode');
    console.log('outside');
  },
  methods: {
    setCity() {
      localStorage.setItem('weatherZipcode', this.zipcode);
      this.$router.push('/weather');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.weatherForm{
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
.form-weather {
  width: 100%;
  max-width: 250px;
  text-align: center;
}
.zipcode-content {
  width: 100%;
}
.zipcode-content input{
  text-align: center;
    margin: 12px 0 20px;
    padding: 10px 0;
    width: 100%;
}
.zipcode-submit input {
  padding: 8px 30px;
  cursor: pointer;
}
</style>