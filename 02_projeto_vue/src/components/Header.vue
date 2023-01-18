<template>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Projetos</a></li>
        <li><a href="#">Contato</a></li>
    </ul>
</template>

<script>
export default {
    name: 'Headers'
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
    color: turquoise;
}
</style>