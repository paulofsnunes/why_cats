<template>
    <v-row
    no-gutters
    class="my-15">
        <v-col
        cols="6"
        md="6"
        class="d-none d-sm-flex d-md_lg_xl-flex"
        offset-md="0"
        >
            <v-img
            contain
            max-height="100%"
            max-width="100%"
            src="/undraw_friends_r511.svg" alt="Menina sentada em um parque com gato um ao lado"
            ></v-img>
        </v-col>
        <v-col
        cols="12"
        sm="6"
        md="6"
        class="align-self-center"
        >
            <p class="mb-n1">Razões para adotar um gato</p>
            <h2>O que torna esses animais tão especiais</h2>
            <div
            class="mb-5">
                <v-row class="mt-5">
                    <v-col>
                        <p class="mb-n1">01</p>
                        <span>Basta um carinho e eles ligam seus motores, melhor que hot wheels.</span>
                    </v-col>
                    <v-col>
                        <p class="mb-n1">02</p>
                        <span>São altamente colecionáveis, monocromáticos, coloridos e até sem pelos.</span>
                    </v-col>
                </v-row>
                <v-row class="mt-5">
                    <v-col>
                        <p class="mb-n1">03</p>
                        <span>Os seres mais fotogênicos do planeta, você vai registar até o sono deles.</span>
                    </v-col>
                    <v-col>
                        <p class="mb-n1">04</p>
                        <span>Limpinhos, eles tomam banho por conta própria, várias vezes ao dia.</span>
                    </v-col>
                </v-row>
                <v-row class="mt-5">
                    <v-col>
                        <p class="mb-n1">05</p>
                        <span>Ótimos padeiros, quando menos se espera eles estão lá fazendo massa.</span>
                    </v-col>
                    <v-col>
                        <p class="mb-n1">06</p>
                        <span>Protetores espirituais, você não precisará mais tapar o umbigo.</span>
                    </v-col>
                </v-row>
            </div>
            <ButtonContact/>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'ReasonsChoose',
}
</script>

<style scoped>
p {
    color: #e06cb9;
}

span {
    color: #5e6697;
    font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
}
</style>