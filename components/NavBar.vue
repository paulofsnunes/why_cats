<template>
    <v-app-bar
    color="white"
    elevation="2"
    height="90"
    >

        <NuxtLink to="/">
            <v-img
            title="Logo"
            src="/Why Cats.png"
            alt="Logo da Why Cats com um gato e a frase 'Why Cats?'"
            max-height="85"
            max-width="85">
            </v-img>
        </NuxtLink>

        <v-spacer></v-spacer>

        <NuxtLink title="Sobre o autor da página" to="/about" class="mr-5 link-hover">Sobre</NuxtLink>
        <NuxtLink title="Contatos do autor da página" to="/contact" class="link-hover">Contato</NuxtLink>

    </v-app-bar>
</template>

<script>
export default {
    name: 'NavBar',
}
</script>

<style scoped>
.link-hover {
    color: #5e6697;
    transition: all 0.2s;
}

.link-hover:hover {
    color: #b48bcc;
    transform: scale(1.1);
    position: relative;
    z-index: 1;
}
</style>