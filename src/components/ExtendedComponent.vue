<!-- ExtendedComponent.vue = Option API Component EXTENDED -->
<template>
  <div style="color: blue">
    <div>
      EXTENDED component: <u>{{ message }}</u>
    </div>
    <div>
      plus <u>{{ extra }}</u> and {{ primitiveExtended }}
    </div>
    <div>user: {{ user }}</div>
    <h4 @click="exampleFuncExtended">
      Click here to call "original" function from "local" function
    </h4>
  </div>
</template>
<script>
import Original from "./BaseComponent.vue";

export default {
  name: "EXTENDoriginal",

  extends: Original,

  props: {
    extra: {
      type: String,
      required: false,
    },
  },
  data() {
    let primitiveExtended = this.primitive + 99;
    return {
      primitiveExtended,
      user: {
        id: 9999,
      },
    };
  },
  methods: {
    exampleFuncExtended() {
      alert(
        this.primitive + "(ok) -- " + this.primitiveExtended + " (does not)"
      );
      this.ORIGINAL_FUNCTION(
        "hello it's me you're looking for - A call to original Sample"
      );
    },
  },
};
</script>