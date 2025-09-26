<template>
  <div id="app">
    <HeaderComponent />
    <div class="Navigation">
      <LogoComponent />
      <NavComponent />
      <SearchComponent />
    </div>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import LogoComponent from './components/LogoComponent.vue'
import NavComponent from './components/NavComponent.vue'
import SearchComponent from './components/SearchComponent.vue'

export default {
  name: "App",
  components: {
    HeaderComponent,
    LogoComponent,
    NavComponent,
    SearchComponent
  }
}
</script>

<style>
.Navigation {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: #e6e6e6;
  padding: 10px 20px;
}
</style>
