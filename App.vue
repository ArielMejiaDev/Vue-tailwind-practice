<template>
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi sitio personal</title>
    <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 h-100">
    
    <div class="container mx-auto p-4">

        <contact-card/>

        <div class="mt-10" v-if="showSkills">

            <h2 class="m-2 font-semibold text-xl text-gray-800">Skills</h2>

            <badge :title="skill.title" :link="skill.link" v-for="(skill, index) in skills" :key="index"/>

        </div>


    </div>

</body>
</html>
</template>

<script>
import ContactCard from './components/ContactCard.vue';
import Badge from './components/Badge.vue';

export default {
    components: {
        ContactCard,
        Badge,
    },
    data() {
        return {
            showSkills: true,
            skills: [
                {
                    "title": "HTML",
                    "link": "https://html.com",
                },
                {
                    "title": "CSS",
                    "link": "https://css.com",
                },
                {
                    "title": "Sass",
                    "link": "https://sass.com",
                },
                {
                    "title": "PHP",
                    "link": "https://php.net",
                },
            ] 
        }
    },
}


</script>

<style>

</style>