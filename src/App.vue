<!-- APP.VUE -->
<template>
  <div id="app">
    <h2>Original/base 'tag': <original message="Test String" /></h2>
    <hr />
    <h2>
      EXTENDED 'tag':
      <EXTENDoriginal message="Have this too" extra="THIS OTHER PROP" />
    </h2>
  </div>
</template>

<script>
import BaseComponent from "./components/BaseComponent.vue";
import ExtendedComponent from "./components/ExtendedComponent.vue";

export default {
  components: {
    original: BaseComponent,
    EXTENDoriginal: ExtendedComponent,
  },
};
</script>