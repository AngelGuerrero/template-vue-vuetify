<template>
  <v-app>
    <!-- Navbar donde se muestra el nombre de usuario -->
    <navbar-account-component></navbar-account-component>

    <!-- Navbar para mostrar el título del sitio -->
    <navbar-title-component></navbar-title-component>

    <!-- Navbar principal -->
    <div>
      <navbar-component color="indigo"></navbar-component>
    </div>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import NavbarAccountComponent from '@/components/Navbar/NavbarAccountComponent'
import NavbarTitleComponent from '@/components/Navbar/NavbarTitleComponent'
import NavbarComponent from '@/components/Navbar/NavbarComponent'

export default {
  name: 'App',

  components: {
    NavbarAccountComponent,
    NavbarComponent,
    NavbarTitleComponent
  }
}
</script>
