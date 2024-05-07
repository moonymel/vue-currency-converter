<script>
export default {
  props: {
    currencies: Object,
  },
  data() {
    return {
      digit: '',
    }
  }
}
</script>

<template lang="">

<input type="text" class="form-control" v-model="digit">
<select name="" id="" class="form-select">
  <option v-for="(currency, key) in currencies" :value="key" :selected="key === 'EUR' ? true : false">{{ currency }}</option>
</select>

</template>

<style lang="">

</style>