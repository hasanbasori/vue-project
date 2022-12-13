<template>
  <h1>name : {{ name }} and salary : {{ salary }}</h1>
</template>

<script>
export default {
  name: 'PersonComponent',

  props: ['name', 'salary'],
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
