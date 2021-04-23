<template>
  <v-app>
    <!-- Navbar principal -->
    <navbar-component color="primary"></navbar-component>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import NavbarComponent from '@/components/Navbar/NavbarComponent'

export default {
  name: 'App',

  components: {
    NavbarComponent
  }
}
</script>
