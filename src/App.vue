<template>
  <div><h1>App Component</h1></div>
  <FormComponent />
  <ListData />
  <ListData />
  <ListData />
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

<style></style>
