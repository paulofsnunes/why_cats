<template>
    <v-row
    no-gutters
    class="my-10">
        <v-col
        cols="12"
        sm="6"
        md="6"
        class="align-self-center"
        >
            <div
            class="col-lg-8"
            >
                <h1>Why Cats?</h1>
                <p>Página idealizada para idolatrar esses felinos ronronantes. Amamos todos os animais, mas como você percebeu os gatos tomaram essa página. Assim como eles tomam seu sofá, sua cama, os lugares mais altos e inesperados da sua casa eles também encontraram uma maneira de fazer parte do mundo virtual.</p>
                <ButtonContact/>
            </div>
        </v-col>
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
            src="/undraw_pet_adoption_-2-qkw.svg" alt="imagem de um homem escolhendo gato para adoção"
            ></v-img>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'PagePresentation'
}
</script>