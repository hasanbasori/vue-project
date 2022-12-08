<template>
  <div class="app">
    <h2 align="left">Name : {{ firstName }}</h2>
    <h2 align="left">Lastname : {{ lastName }}</h2>
    <h2 align="left">age : {{ age }}</h2>
    <p>Address : <span v-html="address"></span></p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Hasanbasori',
      lastName: 'Samang',
      age: 25,
      weigh: 130.5,
      address: '<strong>Bangkok</strong>',
    };
  },
};
</script>
