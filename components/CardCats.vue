<template>
    <v-responsive
        :options="{
        threshold: .5
        }"
        min-height="200"
        transition="fade-transition"
        class="my-15">
        <div class="text-center">
            <div class="d-flex justify-center mb-4">
                <h2>Alguns <span>gatos</span> incríveis</h2>
            </div>
        </div>
        <v-row>
            <v-col
            v-for="cats in catsData"
            :key="cats.id"
            class="d-flex child-flex"
            cols="4"
            >
                <v-hover>
                    <template #default="{ hover }">
                        <div
                        :class="`elevation-${hover ? 5 : 0}`"
                        class="mx-auto pa-2 transition-swing"
                        >
                            <v-img
                                :src="cats.url"
                                :lazy-src="cats.url"
                                aspect-ratio="1"
                                class="grey lighten-2"
                            >
                                <template #placeholder>
                                    <v-row
                                        class="fill-height ma-0"
                                        align="center"
                                        justify="center"
                                    >
                                        <v-progress-circular
                                        indeterminate
                                        color="grey lighten-5"
                                        ></v-progress-circular>
                                    </v-row>
                                </template>
                            </v-img>
                        </div>
                    </template>
                </v-hover>
            </v-col>
        </v-row>
        <v-row
        align="center"
        justify="center">
            <v-btn
            title="Gerar imagens de gatos aleatoriamente"
            text
            icon
            color="purple accent-2"
            class="mb-3"
            @click="getCat"
            ><v-icon large>mdi-restore</v-icon>
            </v-btn>
        </v-row>
    </v-responsive>
</template>

<script>

export default {
    name: 'CardCats',
    data: () => ({
        catsData: {},
        image: {id:"", url: ""},
    }),
    created(){
        this.getCat();
    } ,
    methods: {
        getCat() {
            const axios = require('axios');

            const config = {
            method: 'get',
            url: 'https://api.thecatapi.com/v1/images/search?limit=3',
            headers: { 
                'Content-Type': 'application/json',
                'x-api-key': '24d53fe3-521a-4686-a02b-7c0732e59d15'
            }
        };

        axios(config)
            .then(response => {
            this.catsData = response.data
            })
            .catch(error => {
            alert(error);
            });
        }
    }
} 
</script>

<style scoped>
span {
    color: #e06cb9;
}

.v-btn {
    transition: all 0.2s;
}

.v-btn:hover {
    transform: scale(1.1);
    position: relative;
    z-index: 1;
}
</style>