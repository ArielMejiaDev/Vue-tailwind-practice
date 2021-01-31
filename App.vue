<template>
    <div class="bg-gray-100 h-screen">

        <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">

        <div class="container mx-auto p-4">

            <h1 class="text-gray-700 font-bold text-2xl underline my-10">Personal Site</h1>

                <div class="mt-10" v-if="showSkills">

                <sub-title text="Skills" />

                <badge :title="skill.title" :link="skill.link" v-for="(skill, index) in skills" :key="index"/>

            </div>

            <div class="my-10">
                <sub-title text="Contact" />

                <contact-card/>
            </div>


        </div>

    </div>

</template>

<script>
import SubTitle from './components/SubTitle.vue';
import ContactCard from './components/ContactCard.vue';
import Badge from './components/Badge.vue';

export default {
    components: {
        SubTitle,
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