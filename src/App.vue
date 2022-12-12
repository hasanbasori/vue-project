<template>
  <div class="app">
    <img
      v-bind:src="picture"
      v-bind:width="size"
      :height="size"
      ref="imageURL"
    /><br />

    <h2 align="left">Full name : {{ getFullName }}</h2>
    <h2>age : {{ age }}</h2>
    <h2>Salary (month): {{ salary }} Bath per month</h2>
    <!-- <h2>Salary (year) : {{ getIncome }} Bath per year</h2> -->
    <h1>Position : {{ getPosition }}</h1>

    <button @click="addSalary(1000)">Update Salary</button>
    <h1>Method1 : {{ getRandomByMethod() }}</h1>
    <h1>Method2 : {{ getRandomByMethod() }}</h1>
    <hr />
    <h1>Computed1: {{ getRandomByComputed }}</h1>
    <h1>Computed2 : {{ getRandomByComputed }}</h1>

    <hr />
    <h1>getRandomByComputed2: {{ getRandomByComputed2 }}</h1>

    <button @click="toggleVisible">
      {{ isVisible ? 'Hide Information' : 'More Information' }}
    </button>
    <article v-show="isVisible">
      <p>Address : <span v-html="address"></span></p>
      <p>
        Facebook Link : <a v-bind:href="socialURL" target="_blank">Facebook</a>
      </p>
      <p v-if="hobby.length === 0">No any hobby</p>
      <div v-else>
        <p>Hobby :</p>
        <ul>
          <li v-for="(item, index) in hobby" :key="index">{{ item }}</li>
        </ul>
      </div>
      <p>Personal Information :</p>
      <ul>
        <li v-for="(item, key) in generalInformation" :key="key">
          {{ key }}: {{ item }}
        </li>
      </ul>
    </article>
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
      hobby: [
        'read a book',
        'play a game',
        'listen music',
        'social media',
        'fitness',
        'outdoor exercise',
      ],
      generalInformation: {
        gender: 'male',
        weight: 85,
        height: 175,
        isMarried: false,
        telephoneNumber: '0967073404',
      },
      isVisible: false,
      salary: 26000,
    };
  },

  methods: {
    toggleVisible() {
      this.isVisible = !this.isVisible;
    },
    getRandomByMethod() {
      return Math.random();
    },
    addSalary(values) {
      this.salary += values;
    },
  },
  computed: {
    getFullName() {
      return `${this.firstName + ' ' + this.lastName}`;
    },

    getRandomByComputed() {
      return Math.random();
    },
    getRandomByComputed2() {
      return Math.random();
    },
    getIncome() {
      return this.salary * 12;
    },
    getPosition() {
      return this.salary >= 35000 ? 'Project Manager' : 'Programmer';
    },
  },
  watch: {
    salary(value) {
      if (value > 50000) {
        alert('salary cannot up to 50000 Bath');
        setTimeout(() => {
          this.salary = 20000;
        }, 2000);
      }
    },
  },
};
</script>
