<template>
  <v-container>
    <FontSize/>
    <PagePresentation/>
    <CardCats/>
    <ReasonsChoose/>
    <TheForm/>
  </v-container>
</template>

<script>
export default {
  name: 'IndexPage',
  head() {
    return {
      title: 'Home',
      meta: [
        { hid: 'description', name: 'description', content: 'Página idealizada para idolatrar gatos ou te converter em um amante desses felinos.' },
      ]
    }
  }
}
</script>

<style>
a {
  text-decoration: none;
}

h1, h2 {
  color: #5e6697;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}

p {
  color: #b48bcc;
  font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
</style>