<template>
  <div>{{ message }}</div>
  <Person />
  <Person />
 

</template>

<script>
import Person from './Person.vue';
export default {
  name: 'ListData',
  components: {
    Person,
  },
  data() {
    return {
      message: 'Company Employee Name',
    };
  },
};
</script>

<style></style>
