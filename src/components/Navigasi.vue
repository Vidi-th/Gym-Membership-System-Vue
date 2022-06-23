<template>
    <div>
        <v-navigation-drawer
        v-model="drawer"
        :mini-variant.sync="mini"
        permanent
        color="#FEFEFE"
        app
        >
        <v-list-item class="px-2 pt-1">
            <v-list-item-content>
                <v-img class="navLogo"
                alt="Gym Management Logo"
                contain
                src="@/assets/icon.png"
                max-height="127px"
                width="212px"
                />
            </v-list-item-content>
        </v-list-item>
        <v-list shaped  class="clickable">
            <template v-for="item in items">
            <v-list-group
                v-if="item.children"
                :key="item.text"
                v-model="item.model"
                :prepend-icon="item['icon-ctr']"
                :append-icon="item.model ? item.icon : item['icon-alt']"
                @click="press(item.text)"
                active-class="orange--text"
            >
                <template v-slot:activator>
                <v-list-item-content class="grey--text">
                    <v-list-item-title >
                    {{ item.text }}
                    </v-list-item-title>
                </v-list-item-content>
                </template>
                <v-list-item class="grey--text"
                v-for="(child, i) in item.children"
                :key="i"
                route :to="child.route"
                active-class="orange--text"
                >
                <v-list-item-action v-if="child.icon">
                    <v-icon>{{ child.icon }}</v-icon>
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title>
                    {{ child.text }}
                    </v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </v-list-group>
            <v-list-item class="grey--text"
                v-else
                :key="item.text"
                active-class="orange--text"
                route :to="item.route"
                @click="press(item.text)"
            >
                <v-list-item-action>
                <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-action>
                <v-list-item-content>
                <v-list-item-title>
                    {{ item.text }}
                </v-list-item-title>
                </v-list-item-content>
            </v-list-item>
            </template>  
        </v-list>

        </v-navigation-drawer>

        <v-app-bar
        app
        color="#FEFEFE"
        height="80px"
        >

        <v-icon @click="mini = !mini" class="mr-4">mdi-menu</v-icon>

        <div class="d-flex align-center">
            <v-toolbar-title
            class="judulHalaman"
            > {{this.page}} </v-toolbar-title>
        </div>

        <v-spacer></v-spacer>

        <v-menu offset-y>
            <template v-slot:activator="{ on, attrs }">
            <v-btn text
            v-bind="attrs"
            v-on="on">
                <span class="nameUser mr-2">SuperAdmin</span>
                <v-icon color="#BBBBBB">mdi-account-circle</v-icon>
            </v-btn>
            </template>
            
            <v-list class="d-flex justify">
            <v-list-item-content class="buttonLogout justify">
                <div class="d-flex" @click="logout">
                <v-icon color="#B52260" class="px-5">mdi-logout</v-icon>
                <v-list-item-title class="order-2">LOGOUT</v-list-item-title>
                </div>
            </v-list-item-content>
            </v-list>
        </v-menu>
        </v-app-bar>
      <router-view />
</div>

</template>

<script>

export default {
    data: () => ({
      group: null,
      page: "Dashboard",
      selectedItem: 0,
      items: [
        { icon: 'mdi-view-dashboard', text: 'Dashboard' , route:'/'},
        { icon: 'mdi-badge-account-horizontal-outline', text: 'Data Member' , route:'/DataMember'},
        {
          icon: 'mdi-chevron-up',
          'icon-alt': 'mdi-chevron-down',
          'icon-ctr': 'mdi-dumbbell',
          text: 'Data Kelas',
          model: false,
          children: [
        { text: 'Offline', route:'/DataKelasOffline' },
        { text: 'Online', route:'/DataKelasOnline' },
          ],
        },
        { icon: 'mdi-cart', text: 'Data Pemesanan', route:'/DataPemesanan' },
        { icon: 'mdi-badge-account-horizontal-outline', text: 'Data Pelatih', route:'/DataPelatih' },
        { icon: 'mdi-badge-account-horizontal-outline', text: 'Data Admin', route:'/DataAdmin' },
        { icon: 'mdi-calendar-month', text: 'Jadwal Latihan', route:'/JadwalLatihan' },
        { icon: 'mdi-newspaper-variant', text: 'Berita', route:'/Berita'},
      ],
      drawer: null,
      mini: false,
      fab: false,
    }),
    watch: {
      group () {
        this.drawer = false
      },
    },
    methods :{
        press(title){
            this.page = title;
        },
        logout(){
            localStorage.setItem("authenticated", false);
            this.$router.push({name: "Login" })
        },
  },
  }

</script>

<style>
.buttonLogout:hover{
    background-color: #FEE9CC;
    cursor: pointer;
}

.iconLogout{
    color: #B52260;
}

.v-application .orange--text {
    color: #F48743 !important;
    caret-color: #FEE9CC !important;
    background-repeat: repeat-x;
}

.navLogo .v-image__image, .v-image__placeholder {
    max-width: 70%;
    left: 10%
}

* {
    font-family: 'Poppins', sans-serif;
    font-weight: 600;
    font-size: 18px;
}

.nameUser {
    color: #BBBBBB;
}

.judulHalaman {
    font-size: 34px !important;
}

</style>