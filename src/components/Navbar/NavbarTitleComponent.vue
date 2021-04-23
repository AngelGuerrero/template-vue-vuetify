<template>
  <v-container class="">
    <v-row>
      <v-col cols="2">
        <img src="@/assets/logo.png" style="height: 50px; width: 50px;" />
      </v-col>
      <v-col align-self="center" class="dev">
        <h1 class="dev main__title text-md-right">
          Repositorio Digital del Centro de Tecnología Agroindustrial
        </h1>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'NavbarTitleComponent'
}
</script>

<style lang="scss">
@import '~@/assets/scss/main.scss';
</style>
