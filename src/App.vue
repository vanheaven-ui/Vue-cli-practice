<template>
  <h2>My First Vue App :)</h2>
  <button @click="toggleModal">Show Modal</button>
  <Modal v-if="showModal" @close="toggleModal" theme="sale">
    <h1>Ninja Giveaway!</h1>
    <p>Get your Ninja swag at half price</p>
    <template v-slot:links>
      <a href="#">Signup Now</a>
      <a href="#">More info...</a>
    </template>
  </Modal>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
  name: "App",
  components: { Modal },
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
