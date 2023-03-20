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

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" temporary>
      <!--  -->
    </v-navigation-drawer>

    <v-main class="bg-grey-darken-4">
      <v-container>
        <v-row>
          <template v-for="n in 4" :key="n">
            <v-col class="mt-2" cols="12">
              <strong>Category {{ n }}</strong>
            </v-col>

            <v-col v-for="j in 6" :key="`${n}${j}`" cols="6" md="2">
              <v-sheet height="150">
              </v-sheet>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({ drawer: null }),
}
</script>