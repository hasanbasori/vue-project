<template>
  <FormComponent />
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

