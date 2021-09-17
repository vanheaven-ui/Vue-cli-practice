<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>Modal Title</h1>
      <p>Modal content</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["theme"],
  emits: ["close"],
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>

<style>
.backdrop {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal {
  width: 400px;
  margin: 100px auto;
  padding: 10px;
  text-align: center;
  background-color: white;
  border-radius: 10px;
}

.modal.sale {
  background-color: crimson;
  color: white;
}
</style>