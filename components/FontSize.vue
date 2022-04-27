<template>
    <div class="d-flex justify-end">
        <button title="Aumentar fonte" class="mr-3" @click="largeFontSize">A +</button>
        <button title="Diminuir fonte" @click="mediumFontSize">A -</button>
    </div>
</template>

<script>
export default {
    name: 'FontSize',
    methods: {
            largeFontSize(event) {
            document.getElementById("__nuxt").style.fontSize = "x-large"
        },
            mediumFontSize(event) {
            document.getElementById("__nuxt").style.fontSize = "medium"
        }
    }
}
</script>