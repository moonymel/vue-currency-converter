<script>
import axios from 'axios';
import AppInput from './components/AppInput.vue';

export default {
  components: {
    AppInput,
  },
  data() {
    return {
      apiUrl: 'https://api.frankfurter.app',
      currencies: [],
    }
  },
  created() {
    this.getCurrencies();
  },
  methods: {
    getCurrencies() {
      axios.get(`${this.apiUrl}/currencies`).then((response) => {
        this.currencies = response.data
        console.log(this.currencies)
      })
    }
  }
}
</script>

<template lang="">
  <div class="container my-container">
    <div class="row">

      <div class="col-12">
        prova
      </div>

      <div class="col-6">
        prova2
      </div>

      <div class="col-6">
        prova2
      </div>

      <div class="col-12">
        <AppInput :currencies="currencies" />
      </div>

    </div>
  </div>
</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables.scss' as *;
@use './styles/partials/mixins.scss' as *;

.my-container {
  width: 100%;
  background-color: grey;
  border: 1px solid black;
}
</style>