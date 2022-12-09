<template>
  <div class="app">
    <img
      v-bind:src="picture"
      v-bind:width="size"
      :height="size"
      ref="imageURL"
    /><br />

    <h2 align="left">Full name : {{ getFullName() }}</h2>

    <h2 align="left"></h2>
    <p>Address : <span v-html="address"></span></p>
    <p>
      Facebook Link : <a v-bind:href="socialURL" target="_blank">Facebook</a>
    </p>
    <p v-if="hobby.length === 0">No any hobby</p>
    <div v-else>
      <p>Hobby :</p>
      <ul>
        <li>{{ hobby[0] }}</li>
        <li>{{ hobby[1] }}</li>
        <li>{{ hobby[2] }}</li>
      </ul>
    </div>
    <p>Personal Information :</p>
    <ul>
      <li>Gender: {{ generalInformation.gender }}</li>
      <li>Weight: {{ generalInformation.weight }}</li>
      <li>Height: {{ generalInformation.height }}</li>
      <li>isMarried: {{ generalInformation.isMarried }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      firstName: 'Bearsore',
      lastName: 'Cafe',
      nickName: '',
      age: 25,
      weigh: 130.5,
      address: '<strong>Bangkok</strong>',
      picture: 'https://cdn-icons-png.flaticon.com/512/1077/1077114.png',
      size: 150,
      socialURL: 'https://www.facebook.com/hasanbasori.sa',
      hobby: ['read a book', 'play a game', 'listen music'],
      generalInformation: {
        gender: 'male',
        weight: 85,
        height: 175,
        isMarried: false,
        telephoneNumber: '0967073404',
      },
    };
  },
  methods: {
    getFullName() {
      return `${this.firstName + ' ' + this.lastName}`;
    },
  },
};
</script>
