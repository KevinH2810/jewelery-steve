<template>
  <div>
    <Hero @button-a="handleButtonA" @button-b="handleButtonB" />
  </div>
</template>

<script lang="ts">
// import Vue from "vue";
import Hero from "~/components/Hero.vue";

//export default Vue.extend({});
export default {
  components: {
    Hero,
  },
  methods: {
    handleButtonA() {
      alert("Button A");
    },
    handleButtonB() {
      alert("Button B");
    },
  },
};
</script>
