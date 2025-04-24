<template>
  <v-app>
    <v-app-bar app color="teal darken-3">
      <v-spacer />

      <span class="mr-4">{ $store.state.name }</span>
      <v-btn
        class="px-0 rounded-circle"
        href=""
        min-width="36"
        target="_blank"
        text
      >
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    <v-navigation-drawer app class="teal darken-4">
      <v-list>
        <v-list-item class="pl-2">
          <v-list-item-icon class="ml-0 my-2 mr-3">
            <v-icon x-large>mdi-cloud-circle</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>UMS</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item to="/">
          <v-list-item-icon>
            <v-icon>mdi-home</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>Home</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item to="about">
          <v-list-item-icon>
            <v-icon>mdi-information-outline</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title>About</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <template v-slot:append>
        <div class="pa-2">
          <v-btn block> Logout </v-btn>
        </div>
      </template>
    </v-navigation-drawer>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>
<script lang="ts" setup>

</script>
