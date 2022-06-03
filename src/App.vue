<template>
  <v-app>
    <v-navigation-drawer 
      v-model="drawer"
      fixed
      app
      color="#FEFEFE"
    >
      <v-list-item>
        <div class="d-flex align-center pa-52px">
          <v-list-item-content>
            <v-img
            alt="Gym Management Logo"
            contain
            src="@/assets/Logo.png"
            height="127px"
            width="212px"
          />
          </v-list-item-content>
        </div>
      </v-list-item>


      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="(item, index) in items"
          :key="index"
          @click="press(item.title)"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    
    <v-app-bar
      app
      color="#FEFEFE"
      fixed
    >
    <v-app-bar-nav-icon 
      @click.stop="drawer = !drawer"
      color="#F48743">
    </v-app-bar-nav-icon>

      <div class="d-flex align-center">
        <v-app-bar-title
        class="font-weight-bold"
        > GYM MEMBERSHIP SYSTEM </v-app-bar-title>
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

    data: () => ({
      items: [
        { title: 'Dashboard', icon: 'mdi-view-dashboard' },
        { title: 'Data Admin', icon: 'mdi-badge-account-horizontal-outline' },
        { title: 'Data Member', icon: 'mdi-badge-account-horizontal-outline' },
        { title: 'Classes', icon: 'mdi-dumbbell' },
        { title: 'Newsletter', icon: 'mdi-newspaper-variant' },
        { title: 'Logout', icon: 'mdi-logout' },
      ],
      drawer: false,
      group: null,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>

<style>
.v-main__wrap {
    background-color: #FEE9CC;
}

.v-image__image, .v-image__placeholder {
    max-width: 70%;
}

* {
    justify-content: center;
}



</style>