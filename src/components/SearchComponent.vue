<template>
  <div class="Search">
    <input type="search" v-model="searchQuery" placeholder="search">
  </div>
</template>

<script>
export default {
  name: "SearchComponent",
  data() {
    return {
      searchQuery: ""
    }
  }
}
</script>

<style scoped>
input {
  padding: 5px;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
