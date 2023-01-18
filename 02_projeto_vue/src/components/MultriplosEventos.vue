<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceito()">Ativar Multriplos
            Eventos</button>
        <p>{{ multriplos_eventos }}</p>
    </div>
</template>
<!-- ------------------------ -->
<script>
export default {
    name: 'MultriplosEventos',
    data() {
        return {
            multriplos_eventos: '',
            txt1: '1º Evento',
            txt2: '2º Evento',
        }
    },
    methods: {
        primeiro(txt, e) {
            this.multriplos_eventos = txt
        },
        segundo(txt, e) {
            setTimeout(() => this.multriplos_eventos = txt, 1000)
        },
        terceito(txt, e) {
            setTimeout(() => this.multriplos_eventos = "", 2000)
        }
    }
}
</script>
<!-- ------------------------ -->
<style scoped>
div {
    margin: 100px;
}
</style>