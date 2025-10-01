<template>
  <div id="app">
    <!-- Header -->
    <LogoComponent />
    <HeaderComponent />

    <!-- Navigation -->
    <NavComponent @navigate="currentPage = $event" />

    <!-- Page Content -->
    <main class="page-content">
      <component :is="currentPage" />
    </main>

    <!-- Footer -->
    <footer class="footer">
      <p>© Copyrights 2025 MOTOR HUB. All Rights Reserved. | Privacy Policy & Terms Of Use</p>
      <p>
        This site and the products and services offered on this site are not associated, affiliated, endorsed. All
        trademarks, logos, and service marks (collectively "Trademarks") displayed are registered and/or unregistered
        Trademarks of their respective owners.
      </p>
    </footer>
  </div>
</template>

<script>
import LogoComponent from './components/LogoComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import NavComponent from './components/NavComponent.vue'

// Import each page
import Home from './views/Home.vue'
import Design from './views/Design.vue'
import Features from './views/Features.vue'
import Innovation from './views/Innovation.vue'
import Exclusive from './views/Exclusive.vue'
import Vehicles from './views/Vehicles.vue'
import About from './views/About.vue'
import Contact from './views/Contact.vue'

export default {
  name: "App",
  components: {
    HeaderComponent,
    NavComponent,
    LogoComponent,
    Home,
    Design,
    Features,
    Innovation,
    Exclusive,
    Vehicles,
    About,
    Contact
  },
  data() {
    return {
      currentPage: "Home" // default page
    }
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f9f9f9;
}

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.page-content {
  flex: 1;
  padding: 20px;
  max-width: 1000px;
  margin: auto;
}

.footer {
  text-align: center;
  background: #000;
  color: white;
  padding: 20px;
  margin-top: 20px;
}
</style>
