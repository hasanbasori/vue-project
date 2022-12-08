<template>
  <div class="app">
    <!-- การ biding สามารถที่ขะใช้คำว่า v-bind:src หรือ :src คือความหมายเดียวกัน -->
    <img v-bind:src="picture" v-bind:width="size" :height="size" />
    <h2 align="left">Full name : {{ getFullName() }}</h2>
    <h2 align="left">age : {{ age }}</h2>
    <p>Address : <span v-html="address"></span></p>
    <a v-bind:href="socialURL" target="_blank">Facebook</a>
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
      picture: 'https://cdn-icons-png.flaticon.com/512/1077/1077114.png',
      size: 150,
      socialURL: 'https://www.facebook.com/hasanbasori.sa',
    };
  },
  methods: {
    getFullName() {
      return `${this.firstName + ' ' + this.lastName}`;
    },
  },
};
</script>
