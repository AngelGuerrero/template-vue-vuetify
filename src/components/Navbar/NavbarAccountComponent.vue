<template>
  <v-container fluid class="dev wrapper--bg">
    <v-container class="dev d-flex justify-space-between" align-center>
      <v-btn class="dev wrapper--bg" elevation="0">
        Ayuda
        <v-icon>mdi-help-circle</v-icon>
      </v-btn>

      <div>
        <v-text-field
          class="dev"
          placeholder="Buscar"
          outlined
          background-color="white"
          light
          dense
          clearable
          hide-details
        ></v-text-field>
      </div>

      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn v-bind="attrs" v-on="on" elevation="0" class="wrapper--bg">
            Avanzado
            <v-icon dark right>mdi-chevron-down</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in ['Opción 1', 'Opción 2']"
            :key="index"
          >
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>

      <v-divider class="mx-1" dark vertical></v-divider>

      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn v-bind="attrs" v-on="on" elevation="0" class="wrapper--bg">
            <v-icon class="mr-2">mdi-account</v-icon>
            Alejandro
            <v-icon dark right>mdi-chevron-down</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in ['Perfil', 'Cuenta']"
            :key="index"
          >
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: 'NavbarAccount'
}
</script>

<style lang="scss" scoped>
@import '~@/assets/scss/main.scss';

.wrapper--bg {
  background-color: $accent-400 !important;
  color: white !important;
}
</style>
