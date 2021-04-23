<template>
  <v-app-bar app :color="color" dark>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-toolbar-title>Inicio</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-btn :color="color" elevation="0"> Temas </v-btn>
    <v-divider vertical dark class="mx-2"></v-divider>
    <v-btn :color="color" elevation="0">Libros</v-btn>
    <v-divider vertical class="mx-2"></v-divider>

    <v-menu offset-y>
      <template v-slot:activator="{ on, attrs }">
        <v-btn :color="color" v-bind="attrs" v-on="on" elevation="0">
          Publicaciones
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(item, index) in ['Primera', 'Segunda']"
          :key="index"
        >
          <v-list-item-title>{{ item }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </v-app-bar>
</template>

<script>
export default {
  name: 'NavbarComponent',

  props: {
    color: {
      type: String,
      default: 'primary'
    }
  }
}
</script>

<style lang="scss" scoped></style>
