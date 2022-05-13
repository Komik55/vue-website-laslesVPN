<template>
  <div class="my__select uppercase py-3">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "my-select",
};
</script>
<style scoped>
.my__select {
  padding: 10px 0;
  text-transform: uppercase;
  font-weight: bold;
  border: 1px solid #f53855;
  border-radius: 50px;
  color: #f53855;
  width: 150px;
  position: relative;
  text-align: center;
  cursor: pointer;
}
.my__select:hover {
  background-color: #f53855;
  border: none;
  transition: 1s;
  color: #fff;
}
.my__select:hover::after {
  bottom: -30px;
  content: "";
  left: 0px;
  position: absolute;
  width: 211.83px;
  height: 30px;
  filter: blur(24px);
  background-color: rgba(245, 56, 56, 0.35);
  border-radius: 10px;
}
</style>
