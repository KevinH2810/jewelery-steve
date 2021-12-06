<template>
  <!-- <div>
    <button @click="onClickA">Button A</button>
    <button @click="onClickB">Button B</button>
  </div> -->
  <section class="hero">
    <div class="hero-content">
      <h1 class="hero-title">Discover</h1>

      <h2 class="hero-subtitle">Your Gem</h2>

      <button type="button" class="button-primary" @click="onClickA">
        Button A
      </button>
      <button type="button" class="button-default" @click="onClickB">
        Button B
      </button>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    onClickA() {
      this.$emit("button-a");
    },
    onClickB() {
      this.$emit("button-b");
    },
  },
};
</script>

<style lang="css">
body {
  margin: 0;
  padding: 0;
}

.hero {
  position: relative;
  width: 100vw;
  height: 35vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url(assets/images/main_banner.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center center;
  filter: brightness(60%);
}

.hero-content {
  position: relative;
  font-family: "Monserrat", sans-serif;
  color: white;
  text-align: left;
  margin: 0.625rem;
}

.hero-title {
  font-size: 3rem;
  font-weight: 600;
  margin-bottom: 0;
}

.hero-subtitle {
  font-size: 2rem;
  font-weight: 200;
  margin-top: 1rem;
}

.button-primary {
  background-color: #ae2d59;
  color: white;
  border: 1px solid #cb376a;
  margin-top: 2rem;
  padding: 0.9375rem 1.875rem;
  font-family: "Monserrat", sans-serif;
  font-size: 1.125rem;
  font-weight: 200;
  cursor: pointer;
}

.button-primary:hover {
  background-color: #cb376a;
  border: 1px solid #db7598;
}

.button-default {
  background-color: transparent;
  color: white;
  border: 1px solid #fff;
  margin-top: 2rem;
  padding: 0.9375rem 1.875rem;
  font-family: "Monserrat", sans-serif;
  font-size: 1.125rem;
  font-weight: 200;
  cursor: pointer;
}

.button-default:hover {
  color: #2c3e50;
  background-color: #f8f9f9;
  border: 1px solid #17202a;
}
</style>