<template>
    <v-app>
        <div
        class="mx-auto text-center my-10"
        style="max-width: 500px;">
            <h1>Minhas redes sociais e demais contatos</h1>
        </div>
            <div class="mx-auto">
                <v-list>
                    <v-list-item
                    v-for="(item, i) in items"
                    :key="i"
                    :href="item.href"
                    target="_blank"
                    class="link-item"
                    >
                    <v-list-item-icon>
                        <v-icon v-text="item.icon"></v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                        <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item-content>
                    </v-list-item>
                </v-list>
            </div>
    </v-app>
</template>

<script>
export default {
    name: 'ContactPage',
    data: () => ({
        items: [
            { text: 'linkedin.com/in/paulofsnunes', icon: 'mdi-linkedin', href: 'https://linkedin.com/in/paulofsnunes' },
            { text: 'github.com/paulofsnunes', icon: 'mdi-github', href: 'https://github.com/paulofsnunes' },
            { text: 'paulofsnunes@gmail.com', icon: 'mdi-email-check-outline', href: 'mailto:paulofsnunes@gmail.com' },
            { text: '(51) 99338-3900', icon: 'mdi-whatsapp', href: 'https://wa.me/5551993383900?text=Oi,%20Paulo%0AGostei%20muito%20da%20p%C3%A1gina%20Why%20Cats,%20parab%C3%A9ns!%0ATenho%20interesse%20em%20conversar%20mais%20sobre%20desenvolvimento%20front-end.%20Tens%20um%20tempinho?' },
        ],
    }),
    head() {
        return {
            title: 'Contatos do autor',
            meta: [
                { hid: 'description', name: 'description', content: 'Página com os contatos e redes sociais do autor da Why Cats?' },
            ]
        }
    }
}
</script>

<style scoped>
.link-item {
    transition: transform 0.2s ease-in-out;
}

.link-item:hover {
    transform: scale(1.05);
}
</style>