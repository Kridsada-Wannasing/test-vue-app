<template>
  <div class="bg">
    <AppBar />
    <Jumbotron class="jumbotron-center" />
  </div>
</template>

<script>
import AppBar from "../components/headers/AppBar";
import Jumbotron from "../components/headers/Jumbotron";
export default {
  components: {
    AppBar,
    Jumbotron,
  },
};
</script>

<style scoped>
.bg {
  background-color: gray;
  height: 80vh;
  padding: 0 100px;
}
* {
  color: white;
}
.jumbotron-center {
  transform: translateY(50%);
}
</style>
