<template>
  <div>
    <v-app-bar
      color="deep-purple accent-4"
      dark
    >
      <!-- <v-app-bar-nav-icon></v-app-bar-nav-icon> -->

      <v-toolbar-title>
          <v-btn nuxt to="/" text>
          Course platform</v-btn>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            icon
            v-bind="attrs"
            v-on="on"
          >
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>

        <v-list>
          <v-list-item
            v-for="data in auth"
            :key="data.title"
            @click="() => {}"
            nuxt
            :to="data.route"
          >
            <v-list-item-title> {{ data.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
  </div>
</template>

<script>
export default {
    name: 'appBar',
    data () {
        return {
            auth: [
                {title: 'login', route: '/login'},
                {title: 'register', route: '/register'},
            ]
        }
    }
}
</script>