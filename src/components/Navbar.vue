<script setup>
import DarkModeButton from './DarkModeButton.vue';
</script>

<template>
    <section id="navbar"
        class="dark:text-slate-300 i-transtition duration-200 shadow-sm hover:shadow py-7 text-3xl text-slate-600 flex justify-center items-center border-t-2 border-blue-500 dark:border-pink-600 dark:shadow dark:hover:shadow-md">
        <div class="w-full px-6 lg:max-w-5xl flex flex-row flex-nowrap justify-between items-center">
            <a class="font-bold cursor-default hover:text-sky-400 i-transtition duration-300">iYuan's Lab</a>

            <DarkModeButton />
        </div>
    </section>
</template>