<template>
    <Popover as="div" class="relative">
        <PopoverButton>
            <div class="inline-flex justify-center rounded p-2 hover:bg-slate-200 dark:hover:bg-slate-700 duration-300 transition-all">
                <MoonIcon class='w-6 h-6' />
            </div>
        </PopoverButton>

        <transition enter-active-class="transition duration-200 ease-out" enter-from-class="translate-y-1 opacity-0"
            enter-to-class="translate-y-0 opacity-100" leave-active-class="transition duration-150 ease-in"
            leave-from-class="translate-y-0 opacity-100" leave-to-class="translate-y-1 opacity-0">
            <PopoverPanel as="div"
                class="flex flex-col text-base font-semibold text-left justify-center mt-1 z-10 absolute bg-white rounded-lg right-0 w-32 shadow-lg overflow-hidden border-slate-300 border dark:bg-slate-700 dark:border-slate-700 dark:text-slate-100">

                <button v-if="boolSystemMode" @click="turnSysMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 !text-sky-600 dark:hover:bg-slate-600">
                    <AdjustmentsIcon class="w-6 h-6 mr-2" />
                    跟随系统
                </button>
                <button v-else @click="turnSysMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 dark:hover:bg-slate-600">
                    <AdjustmentsIcon class="w-6 h-6 mr-2" />
                    跟随系统
                </button>

                <button v-if="boolLightMode" @click="turnLightMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 !text-sky-600 dark:hover:bg-slate-600">
                <SunIcon class="w-6 h-6 mr-2" />
                    浅色模式
                </button>
                <button v-else @click="turnLightMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 dark:hover:bg-slate-600">
                <SunIcon class="w-6 h-6 mr-2" />
                    浅色模式
                </button>
                    
                <button v-if="boolDarkMode" @click="turnDarkMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 !text-sky-600 dark:hover:bg-slate-600">
                    <MoonIcon class="w-6 h-6 mr-2" />
                    深色模式
                </button>
                <button v-else @click="turnDarkMode()" class="flex items-center justify-center hover:bg-slate-300 p-3 py-2 dark:hover:bg-slate-600">
                    <MoonIcon class="w-6 h-6 mr-2" />
                    深色模式
                </button>

            </PopoverPanel>

        </transition>
    </Popover>
</template>

<script setup>
import { ref } from 'vue';

const boolDarkMode = ref(false);
const boolLightMode = ref(false);
const boolSystemMode = ref(false);

function checkMode(){
    if (localStorage.theme == undefined){
        boolSystemMode.value = true;
        boolDarkMode.value = false;
        boolLightMode.value = false;
        if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark')
        } else {
            document.documentElement.classList.remove('dark')
        }
    }else if(localStorage.theme == 'dark'){
        boolSystemMode.value = false;
        boolDarkMode.value = true;
        boolLightMode.value = false;
        document.documentElement.classList.add('dark');
    }else if(localStorage.theme == 'light'){
        boolSystemMode.value = false;
        boolDarkMode.value = false;
        boolLightMode.value = true;
        document.documentElement.classList.remove('dark');
    }
}

function turnDarkMode() {
    localStorage.theme = 'dark';
    checkMode();
}

function turnLightMode() {
    localStorage.theme = 'light';
    checkMode();
}

function turnSysMode(){
    localStorage.clear();
    checkMode();
}

checkMode();

import { Popover, PopoverButton, PopoverPanel } from '@headlessui/vue'
import { MoonIcon, AdjustmentsIcon, SunIcon } from '@heroicons/vue/outline';
</script>
