<template>
  <v-app>
      <v-main>
        <router-view />
      </v-main>
  </v-app>
</template>

<script>
export default {
  // components: { NavBarDataKelas },
  name: 'App',
  }
</script>

<style>
.v-main__wrap {
    background-color: #FEE9CC;
}

* {
    justify-content: center;
    font-weight: 600;
}

.navIcon{
  max-height: 40px;
  max-width: 224px;
}

.expansion .v-expansion-panels{
  max-height: 40px;
  max-width: 224px;
}
</style>