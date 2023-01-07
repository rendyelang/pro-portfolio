<template>
    <header class="bg-slate-900 font-body py-3 fixed w-full z-10">
        <nav class="container ">
            <!-- Navigation for lg (laptop) -->
            <div class="hidden lg:block">
                <div class="flex items-center">
                    <nuxt-link class="text-white mr-20 tracking-[0.4em] text-[22px]" to="/">NINJA KEN</nuxt-link>
                    <ul class="inline-flex text-slate-300 text-sm gap-x-5">
                        <nuxt-link class="focus:font-bold focus:text-white" to="#about">Tentang Saya</nuxt-link>
                        <nuxt-link class="focus:font-bold focus:text-white" to="#project">Proyek Contoh</nuxt-link>
                        <nuxt-link class="focus:font-bold focus:text-white" to="#contact">Hubungi Saya</nuxt-link>
                    </ul>
                </div>
            </div>

            <!-- Navigation for hp-tablet -->
            <div class="lg:hidden">
                <div class="flex justify-between">
                    <nuxt-link class="text-white mr-20 tracking-[0.4em] text-[22px]" to="/">NINJA KEN</nuxt-link>
                    <svg @click="show = !show" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        stroke-width="1.5" stroke="currentColor" class="w-9 h-9 text-white block lg:hidden">
                        <path stroke-linecap="round" stroke-linejoin="round"
                            d="M3.75 6.75h16.5M3.75 12h16.5M12 17.25h8.25" />
                    </svg>
                </div>
            </div>

        </nav>
    </header>
    <Transition name="view">
        <div v-show="show" class="fixed z-[100] block lg:hidden">
            <div
                class="text-white absolute flex flex-col h-[100vh] bg-black bg-opacity-80 w-[250px] box-border px-10 py-14 text-lg">
                <div class="absolute top-4 right-4">
                    <svg @click="show = !show" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                        stroke-width="1.5" stroke="currentColor" class="w-7 h-7 font-bold">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                </div>
                <nuxt-link class="focus:font-bold mb-4 text-center" to="#about">Tentang Saya</nuxt-link>
                <nuxt-link class="focus:font-bold mb-4 text-center" to="#project">Proyek Contoh
                </nuxt-link>
                <nuxt-link class="focus:font-bold text-center" to="#contact">Hubungi Saya</nuxt-link>
            </div>
        </div>
    </Transition>
</template>
<script>
export default {
    data() {
        return {
            show: false,
        }
    },
}
</script>
<style>
.view-enter-active,
.view-leave-active {
    transition: opacity 0.5s ease-in-out, transform 0.5s ease;
}

.view-enter-active {
    transition-delay: 0s;
}

.view-enter-from,
.view-leave-to {
    opacity: 0;
    transform: translateX(-100px);
}

.view-enter-to,
.view-leave {
    opacity: 1;
    transform: translateX(0px);
}
</style>