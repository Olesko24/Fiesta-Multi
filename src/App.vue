<template>
  <v-app>
    <NavigationBar @ButtonClicked="handleNavigationButton"/>
    <Form v-bind:aComponent="activeComponent"/>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';

import NavigationBar from './components/NavigationBar.vue';
import Form from './components/Form.vue';
export default Vue.extend({
  name: 'App',

  data: () => ({
    activeComponent: 'Home'
  }),
  methods: {
    handleNavigationButton(component: string){
      this.activeComponent = component;
    }
  },
  components: {
    NavigationBar,
    Form,
  },
});
</script>
