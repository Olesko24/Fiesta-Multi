<template>
    <component :is="activeComponent" />
</template>
<script lang="ts">
import Vue from 'vue';
import Home from './Home.vue';
import Settings from './Settings.vue';
import Overview from './Overview.vue';
export default Vue.extend({
  name: 'Form',
  props: {
    aComponent: String,
  },
  computed: {
    activeComponent: {
      get(): string {
        if (this.aComponent === '' || !this.aComponent) {
          return 'Home';
        } else {
          return this.aComponent;
        }
      },
    },
  },
  mounted() {
    console.log(this.aComponent);
  },
  components: {
    Home,
    Settings,
    Overview,
  },
});
</script>
<style></style>
