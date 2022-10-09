<!-- BaseComponent.vue = Option API Component -->
<template>
  <div style="color: red">
    <div>Original component: {{ message }}</div>
    <div>{{ user }}</div>
  </div>
</template>

<script>
export default {
  name: "original",

  props: {
    message: {
      type: String,
      required: false,
    },
  },
  data() {
    return {
      primitive: 1,
      user: {
        name: "Jack",
        id: 1111,
      },
    };
  },
  methods: {
    ORIGINAL_FUNCTION(val) {
      alert(val);
    },
  },
};
</script>
