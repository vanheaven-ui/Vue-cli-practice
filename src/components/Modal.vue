<template>
  <div class="backdrop">
    <div class="modal">
      <h2>Modal Title</h2>
      <p>Modal content</p>
    </div>
  </div>
</template>

<script>
export default {};
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
</style>