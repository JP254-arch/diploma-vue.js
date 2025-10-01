<template>
  <div class="logo">
    <img src="/public/images/logo.jpg" alt="MotorHub Logo" class="logo-img" />
  </div>
</template>

<script>
export default {
  name: "LogoComponent",
};
</script>

<style scoped>
.logo {
  display: flex;
  justify-content: center; /* centers horizontally */
  align-items: center;     /* centers vertically if parent has height */
  width: 100%;
  padding: 20px 0;
  background-color: white;
}

.logo-img {
  width: 120px;  /* adjust size */
  height: auto;
  object-fit: contain;
}
</style>
