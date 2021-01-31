<template>
    <a :href="link" target="_blank" class="bg-pink-300 text-pink-600 rounded-full inline px-3 py-1 mx-1">
        {{ title }}
    </a>
</template>

<script>

export default {
    props: {
        title: String,
        link: String,
    }
}

</script>

<style>

</style>