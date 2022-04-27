<template>
    <NuxtLink title="Entre em contato" to="#contact" class="white--text btn-contact">Entre em Contato</NuxtLink>
</template>

<script>
export default {
    name: 'ButtonContact',
}
</script>

<style>
.btn-contact {
    background: #e06cb9;
    color: #fff;
    height: 45px;
    min-width: 64px;
    padding: 10px 25px;
    font-size: 16px;
    transition: all 0.2s;
}
.btn-contact:hover {
    background: #b48bcc;
    box-shadow: 0 6px 12px #5e6697;
    transform: scale(1.1);
    position: relative;
    z-index: 1;
}
</style>