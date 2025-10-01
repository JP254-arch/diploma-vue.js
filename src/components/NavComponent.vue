<template>
  <nav class="navigation">
    <ul>
      <li><a href="#" @click.prevent="$emit('navigate', 'Home')">Home</a></li>
      <!-- <li><a href="#" @click.prevent="$emit('navigate', 'Design')">Design</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'Features')">Features</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'Innovation')">Innovation</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'Exclusive')">Exclusive</a></li> -->
      <li><a href="#" @click.prevent="$emit('navigate', 'Vehicles')">Vehicles</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'About')">About Us</a></li>
      <li><a href="#" @click.prevent="$emit('navigate', 'Contact')">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavComponent"
}
</script>

<style scoped>
.navigation ul {
  list-style: none;
  display: flex;
  gap: 20px;
  justify-content: center;
  padding: 10px;
  background: #e6e6e6;
}

a {
  text-decoration: none;
  color: black;
  font-weight: bold;
  cursor: pointer;
}

a:hover {
  color: #42b983;
}
</style>
