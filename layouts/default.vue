<template>
    <div>
        <Header />
        <main>
            <slot></slot>
        </main>
        <Footer />
    </div>
</template>
<script>
import Footer from '~~/components/footer.vue';
import Header from '~~/components/header.vue';
export default {
    components: { Header, Footer }
}
</script>
<style>

</style>