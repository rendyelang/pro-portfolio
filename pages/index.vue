<template>
    <div>
        <Hero />
        <About />
        <Project />
        <Contact />
    </div>
</template>
<script>
import About from '~~/components/About.vue';
import Hero from '~~/components/Hero.vue';
import Project from '~~/components/Project.vue';
import Contact from '~~/components/Contact.vue';

export default {
    components: { Hero, About, Project, Contact }
}
</script>
<style>

</style>