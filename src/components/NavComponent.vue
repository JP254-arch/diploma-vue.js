<template>
  <nav class="navigation">
    <ul>
      <li><a href="#" @click.prevent="$emit('navigate', 'Home')">Home</a></li>
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
/* Navbar container */
.navigation {
  background: #ffffff;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  padding: 15px 30px;
  position: sticky;
  top: 0;
  z-index: 1000;
}

/* Navbar list */
.navigation ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 30px;
  margin: 0;
  padding: 0;
}

/* Navbar links */
.navigation a {
  text-decoration: none;
  font-size: 1rem;
  font-weight: 600;
  color: #333;
  padding: 8px 12px;
  border-radius: 6px;
  transition: all 0.3s ease;
}

/* Hover effect */
.navigation a:hover {
  background: #f0f0f0;
  color: #d43a34;
}

/* Active/Focus state */
.navigation a:focus,
.navigation a:active {
  color: #ffffff;
  background: #d43a34;
}

/* Responsive for mobile */
@media (max-width: 768px) {
  .navigation ul {
    flex-direction: column;
    gap: 15px;
  }
}
</style>
