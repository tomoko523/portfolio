<template>
  <div id="app">
    <v-app light>
      <main>
        <v-content>
          <router-view></router-view>
          <v-footer class="red lighten-2 pa-3 white--text">
            <v-spacer></v-spacer>
            <div>© {{ new Date().getFullYear() }} tomoko523</div>
          </v-footer>
        </v-content>
      </main>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>
