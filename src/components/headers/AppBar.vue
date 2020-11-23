<template>
  <nav class="navbar px-10 pt-5">
    <a href="#" class="link">LOGO</a>

    <ul class="nav-ul">
      <li v-for="(nav, i) in navArr" :key="i" class="mr-6">
        <a class="link" href="#">{{ nav }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      navArr: ["Tickets", "Film List", "News", "Contact"],
    };
  },
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
}
.nav-ul {
  list-style: none;
  display: flex;
}
.link {
  text-decoration: none;
  color: white;
}
</style>
