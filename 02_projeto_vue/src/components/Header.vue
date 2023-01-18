<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
        <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
    </ul>
</template>

<script>
export default {
    name: 'Headers',
    props: ["esta_logado"]
}
</script>

<style scoped>
ul {
    list-style: none;
    display: flex;
    background: #000;
    font-size: 42px;
}

li {
    margin-right: 10px;
    color: #ddd;
}

a {
    color: #ddd;
    text-decoration: none;
    transition: 1.0s;
}

a:hover {
    color: red;
}
</style>