<template>
  <v-app id="inspire">
    <v-system-bar class="bg-grey-darken-4">
      <v-spacer></v-spacer>

      <v-icon icon="mdi-wifi-strength-4"></v-icon>
      <v-icon icon="mdi-signal" class="ms-2"></v-icon>
      <v-icon icon="mdi-battery" class="ms-2"></v-icon>

      <span class="ms-2">3:13PM</span>
    </v-system-bar>

    <v-app-bar class="bg-purple-darken-4">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Test</v-toolbar-title>
    </v-app-bar>
    <v-navigation-drawer
        image="./assets/pat.png"
        permanent
        theme="dark"
        v-model="drawer" temporary
      >
      <v-list>
          <v-list-item
            prepend-avatar="./assets/picOfMe.jpg"
            title="Sieben Nicola"
            subtitle="sieben.nicola@gmail.com"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>
        <v-list nav>
          <v-list-item prepend-icon="mdi-home"><RouterLink class="nav-link text-light pt-4" to="/">Home</RouterLink>
      </v-list-item>
          <v-list-item prepend-icon="mdi-account-supervisor-circle" ><RouterLink class="nav-link text-light pt-4" to="/products">Products</RouterLink></v-list-item>
          <v-list-item prepend-icon="mdi-clock-start" title="Clock-in" value="clockin"></v-list-item>
        </v-list>
      </v-navigation-drawer>
    <router-view />
  </v-app>
</template>

<script>
import { RouterLink } from 'vue-router'
export default {
  data: () => ({ drawer: null }),
}

</script>
