<script setup>
import { Head, Link } from '@inertiajs/inertia-vue3';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
});
</script>

<template>
    <Head title="Welcome" />

    <div class="relative flex items-top justify-center min-h-screen bg-gray-100 dark:bg-gray-900 sm:items-center sm:pt-0">
        <section>
            <h1 class="text-gray-200 text-center text-7xl mb-4">Welcome to OpenChannel</h1>
            <p class="text-gray-400 text-3xl mx-auto  max-w-2xl">OpenChannel is a social media platform where you can connect with friends and share your interests.</p>

            <div class="max-w-6xl mx-auto sm:px-6 lg:px-8">
                <div class="flex justify-center pt-8">
                    <Link
                        :href="route('login')"
                        class="relative inline-flex items-center justify-center p-0.5 mb-2 mr-4 overflow-hidden text-xl font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-purple-600 to-blue-500 group-hover:from-purple-600 group-hover:to-blue-500 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800"
                    ><span class="relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">Log in</span>
                    </Link>
                    <Link
                        v-if="canRegister"
                        :href="route('register')"
                        class="relative inline-flex items-center justify-center p-0.5 mb-2 mr-4 overflow-hidden text-xl font-medium text-gray-900 rounded-lg group bg-gradient-to-br from-purple-600 to-blue-500 group-hover:from-purple-600 group-hover:to-blue-500 hover:text-white dark:text-white focus:ring-4 focus:outline-none focus:ring-blue-300 dark:focus:ring-blue-800"
                    ><span class="relative px-5 py-2.5 transition-all ease-in duration-75 bg-white dark:bg-gray-900 rounded-md group-hover:bg-opacity-0">Sign up</span>
                    </Link>
                </div>
            </div>
        </section>
    </div>
</template>
