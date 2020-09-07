<template>
    <v-footer>
        <v-row justify="center" no-gutters>
            <v-btn text rounded class="ma-2" @click="emitButton('Overview')"><v-icon left>fas fa-globe</v-icon>Übersicht</v-btn>
            <v-btn text rounded class="ma-2" @click="emitButton('Settings')"><v-icon left>fas fa-hammer</v-icon>Einstellungen</v-btn>
        </v-row>
    </v-footer>
</template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  name: 'NavigationBar',
  methods: {
      emitButton(component: string){
          this.$emit('ButtonClicked', component)
      }
  }
});
</script>
