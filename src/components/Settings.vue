<template>
  <div>
    <h2>Einstellungen</h2>
    <br />
    <v-file-input label="Pfad zur Fiesta Datei" placeholder="C:/Programme/Fiesta.bin"/>
  </div>
</template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend({
  name: 'Settings',
});
</script>
