<template>
  <h2>My First Vue App :)</h2>
  <button @click="toggleModal">Show Modal</button>
  <button @click="toggleModalTwo">Show ModalTwo</button>
  <div v-if="showModal">
    <Modal @close="toggleModal" theme="sale">
      <h1>Ninja Giveaway!</h1>
      <p>Get your Ninja swag at half price</p>
      <template v-slot:links>
        <a href="#">Signup Now</a>
        <a href="#">More info...</a>
      </template>
    </Modal>
  </div>
  <div v-if="showModalTwo">
    <Modal @close="toggleModalTwo">
      <h1>Signup to the newsletter</h1>
      <p>For pomos and latest news</p>
    </Modal>
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
  name: "App",
  components: { Modal },
  data() {
    return {
      showModal: false,
      showModalTwo: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo;
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
