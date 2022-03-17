<template>
    <div class="botons">
        <button @click="$emit('prev')">Anterior</button>
        <button @click="$emit('seg')">Següent</button>
    </div>
</template>


<script>
export default {
    name: 'Botons',
}
</script>


<style scoped>
.botons{
    width: 100%;
    display: flex;
}
button {
    width: 100%;
    height: 4rem;
    font-size: 1.5rem;
}
</style>>
