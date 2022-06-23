<template>
  <div class="home">
    <LoginHalaman msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import LoginHalaman from "@/components/LoginHalaman.vue";

export default {
  name: "Home",
  components: {
    LoginHalaman,
  },
};
</script>