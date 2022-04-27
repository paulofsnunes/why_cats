<template>
    <v-footer
        padless
    >
        <v-card
        flat
        tile
        class="bg-footer white--text text-center"
        >
        <v-card-text>
            <v-btn
            v-for="icon in icons"
            :key="icon.id"
            :href="icon.url"
            :target="icon.target"
            class="mx-4 white--text"
            icon
            >
                <v-icon size="24px">
                    {{ icon.name }}
                </v-icon>
            </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0">
            <span class="font-italic">"O gato não oferece serviços. Ele se oferece. Claro que ele quer carinho e abrigo. O amor não é de graça. Como todas as criaturas puras, os gatos são pragmáticos."&nbsp;</span>
            - William S. Burroughs
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
            {{ new Date().getFullYear() }} — <strong>Why Cats?</strong>
        </v-card-text>
        </v-card>
    </v-footer>
</template>

<script>
    export default {
        name: 'TheFooter',
        data: () => ({
            icons: [
                {
                    name:'mdi-facebook',
                    url: 'https://www.facebook.com/',
                    target: '_blank'
                },
                {
                    name:'mdi-twitter',
                    url: 'https://www.twitter.com/',
                    target: '_blank'
                },
                {
                    name:'mdi-linkedin',
                    url: 'https://www.linkedin.com/',
                    target: '_blank'
                },
                {
                    name:'mdi-instagram',
                    url: 'https://www.instagram.com/',
                    target: '_blank'
                }
            ],
        }),
    }
</script>

<style>
.v-footer {
    display: block;
}

.bg-footer {
    background: #5e6697 !important;
}
</style>