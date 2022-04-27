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
            { text: 'linkedin.com/in/paulofsnunes', icon: 'mdi-linkedin' },
            { text: 'github.com/paulofsnunes', icon: 'mdi-github' },
            { text: 'paulofsnunes@gmail.com', icon: 'mdi-email-check-outline' },
            { text: '(48) 98800-7674', icon: 'mdi-whatsapp' },
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