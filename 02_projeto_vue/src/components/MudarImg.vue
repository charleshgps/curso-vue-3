<template>
    <div>
        <button @click="$emit('mudarImg')">Trocar Imagem de Perfil</button>
    </div>
</template>

<script>
export default {
    name: "MudarImg",
    emits: ["mudarImg"]
}
</script>