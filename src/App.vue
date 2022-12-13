<template>
  <h1><h1>App Component</h1></h1>
  <FormComponent />
  <ListData />
  <ListData />
  <ListData />
</template>

<script>
import FormComponent from './components/FormComponent.vue';
import ListData from './components/ListData.vue';
export default {
  name: 'app',
  components: {
    ListData,
    FormComponent,
  },
};
</script>

<style scoped>
h1 {
  background-color: aqua;
}
</style>
