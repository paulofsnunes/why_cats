<template>
  <v-app>
    <NavBar/>
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>
    <TheFooter/>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
