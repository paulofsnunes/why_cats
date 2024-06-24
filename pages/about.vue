<template>
    <v-app>
        <div
        class="mx-auto text-center my-10"
        style="max-width: 500px;">
            <h1 class="mb-5">Olá, seja muito bem vindo</h1>
            <p>Eu me chamo Paulo Franklin e sou o criador da landing page <strong>Why Cats?</strong>.</p>
            <p>Espero que você tenha gostado de visitar a page e, acima de tudo, passasse a idolatrar muito os felinos.</p>
            <p>Bom, eu decidi que essa aba da página fosse dedicada a falar um pouco sobre mim, quem eu sou, minha carreira e aonde quero chegar.</p>
            <p>Sou natural de Porto Alegre/RS, onde resido até o presente momento com minha esposa e meus dois enteados. Nasci em 21 de maio de 1989, em uma linda noite de domingo, para não atrapalhar o final de semana de ninguém. Sou formado em Direito pela PUCRS, concluído em 2013, e em Análise e Desenvolvimento de Sistemas pela Univali, finalizado em 2023.</p>
            <p>Trabalho desde os meus 16 anos de idade, sempre lidando com metas, prazos, alta demanda e por muitas vezes contato direto com clientes.</p>
            <p>Desde sempre demonstrei facilidade em áreas coligadas a tecnologia, principalmente a ciência da computação, a qual se mostrava muito intuitiva para mim. E foi no transcorrer do ano de 2020, no auge da pandemia do Coronavírus, que me encantei pela área de programação e desenvolvimento web. Comecei minha transição de carreira de uma forma a qual nunca tinha me inspirado antes.</p>
            <p>Sou curioso por natureza, adaptável, proativo e amo tecnologia. Estou constantemente me aperfeiçoando, realizando cursos e participando de bootcamps, principalmente com ênfase em front-end, uma paixão.</p>
            <p>Meu objetivo, é um dia ser referência no desenvolvimento web, uma pessoa sempre disposta e capaz de auxiliar o time, ser o líder técnico que eu como júnior gostaria de ter tido ao meu lado.</p>
        </div>
        <div class="d-flex justify-center">
            <v-img
            contain
            max-height="50%"
            max-width="50%"
            src="/playing.svg" alt="Gato feliz brincando na grama"
            ></v-img>
        </div>
    </v-app>
</template>

<script>
export default {
    name: 'AboutPage',
    head() {
        return {
            title: 'Sobre o autor',
            meta: [
                { hid: 'description', name: 'description', content: 'Página dedicada a falar um pouco sobre o autor da Why Cats?' },
            ]
        }
    }
}
</script>