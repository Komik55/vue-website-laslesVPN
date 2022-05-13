<template>
  <button class="btn uppercase py-3">
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: "my-button",
};
</script>
<style scoped>
.btn {
  position: relative;
  border-radius: 10px;
  width: 250px;
  background: #f53838;
  border: none;
  font-weight: 700;
  color: #fff;
}
.btn:hover {
  transition: 0.6s;
  opacity: 0.7;
}
.btn:focus {
  outline: 0;
}
.btn::after {
  bottom: -30px;
  content: "";
  left: 17px;
  position: absolute;
  width: 211.83px;
  height: 30px;
  filter: blur(24px);
  background-color: rgba(245, 56, 56, 0.35);
  border-radius: 10px;
}
</style>
