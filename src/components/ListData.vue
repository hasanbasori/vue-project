<template>
  <div>{{ message }}</div>
  <Person name="sun" salary="16000" />
  <Person name="abdul" salary="26000" />
  <Person name="leeLee" salary="36000" />
  <Person name="same" salary="46000" />
</template>

<script>
import Person from './Person.vue';
export default {
  name: 'ListData',
  components: {
    Person,
  },
};
</script>

<style></style>
