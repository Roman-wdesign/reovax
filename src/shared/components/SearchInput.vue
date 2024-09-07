<script setup>
const props = defineProps({
    label: String
});
</script>

<template>
    <div>
        <input class="input" :placeholder="props.label" />
    </div>
</template>

<style scoped>
.input {
    width: 21.5rem;
    height: 4.6rem;
    padding: 2.8rem 1.2rem 2.8rem 1.2rem;
    background-color: #FFF7F3;
    font-size: 1.6rem;
    color: #F95707;
    border-radius: 10rem;
    border: none;
}
</style>