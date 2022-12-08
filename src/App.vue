<template>
  <div class="app">
    <h2 align="left">Full name : {{ getFullName() }}</h2>
    <h2 align="left">age : {{ age }}</h2>
    <p>Address : <span v-html="address"></span></p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Bearsore',
      lastName: 'Cafe',
      age: 25,
      weigh: 130.5,
      address: '<strong>Bangkok</strong>',
    };
  },
  methods: {
    getFullName() {
      return `${this.firstName + " " + this.lastName}`
    },
  },
};
</script>
