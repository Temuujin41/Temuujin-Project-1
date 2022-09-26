<template>
  <link rel="stylesheet" href="style.css" />
  <div style="margin: 5%">
    <h1>Home</h1>
    <h2>Temuujin's Project</h2>
    <br>
    <button @click="toggleShowbooks">
      <span>Hide</span>
      <span>Show</span>
    </button>
    <Transition>
    <div class="m-8" v-if="Showbooks">
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quidem,
        dolores numquam rerum inventore eius animi!
      </p>
    </div>
  </Transition>
    
  </div>
</template>
<script>
export default {
  data() {
    return {
      Showbooks: true,
      title: " Error",
    };
  },
  methods: {
    toggleShowbooks() {
      this.Showbooks = !this.Showbooks;
    },
  },
};
</script>

<style>
  .v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>