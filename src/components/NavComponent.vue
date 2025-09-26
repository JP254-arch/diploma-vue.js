<template>
  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Design</a></li>
      <li><a href="#">Features</a></li>
      <li><a href="#">Innovation</a></li>
      <li><a href="#">Exclusive</a></li>
      <li><a href="#">Vehicles</a></li>
      <li><a href="#">About Us</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavComponent"
}
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  gap: 20px;
}

a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}

a:hover {
  color: #555;
}
</style>
