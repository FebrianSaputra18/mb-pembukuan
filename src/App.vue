<template>
  <v-app id="inspire">
    <v-navigation-drawer style="background-color: #bcbcbc" v-model="drawer" app>
      <v-list-item style="background-color: sandybrown">
        <v-list-item-content style="height: 128px" color="accent">
          <v-list-item-title class="text-h6"> Rama Sano </v-list-item-title>
          <v-list-item-subtitle> 087788631832 </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
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
      absolute
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="https://cdn.vuetifyjs.com/images/parallax/material.jpg"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to top right, rgba(19,84,122,.5), rgba(128,208,199,.8)"
        ></v-img>
      </template>

      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-app-bar-title>MB Pembukuan</v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-bell</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main style="background-color: #bcbcbc">
      <v-sheet class="overflow-y-auto">
        <v-container>
          <v-row dense>
            <v-col cols="12">
              <v-card color="#82b1ff" dark>
                <v-card-title class="text-h5"> Pembukuan Perhari </v-card-title>

                <v-card-actions>
                  <v-btn text> Buat Sekarang </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>

            <v-col cols="12">
              <v-card color="#f35f1b" dark>
                <v-card-title class="text-h5">
                  Pembukuan Perminggu
                </v-card-title>

                <v-card-actions>
                  <v-btn text> Buat Sekarang </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>

            <v-col cols="12">
              <v-card color="#acent" dark>
                <v-card-title class="text-h5" color="#0000000">
                  Pembukuan Perbulan
                </v-card-title>

                <v-card-actions>
                  <v-btn text> Buat Sekarang </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>

            <v-col cols="12">
              <v-card color="#53a66f" dark>
                <v-card-title class="text-h5">
                  Lihat Grafik Penjualan
                </v-card-title>

                <v-card-actions>
                  <v-btn text> Lihat Sekarang </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-container>
      </v-sheet>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      drawer: false,
      items: [
        { title: "Home", icon: "mdi-home-city" },
        { title: "My Account", icon: "mdi-account" },
        { title: "Users", icon: "mdi-account-group-outline" },
      ],
    };
  },
};
</script>
