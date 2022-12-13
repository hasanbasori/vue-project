<template>
  <h1>{{ message }}</h1>
</template>

<script>
export default {
  name: 'PersonComponent',
  data() {
    return {
      message: 'employee Information',
    };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
