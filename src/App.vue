<template>
    <div id="app">
        <header class="text-gray-600 body-font">
            <div class="container mx-auto flex flex-wrap p-5 flex-col md:flex-row items-center">
                <a class="flex title-font font-medium items-center text-gray-900 mb-4 md:mb-0">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-10 h-10 text-white p-2 bg-indigo-500 rounded-full" viewBox="0 0 24 24">
                        <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path>
                    </svg>
                    <span class="ml-3 font-bold text-xl">Todo App</span>
                </a>
                <nav class="md:ml-auto flex flex-wrap items-center text-base justify-center">
                    <router-link to="/" class="mr-5 text-sm hover:text-gray-900">Home</router-link>
                    <router-link to="/about" class="mr-5 text-sm hover:text-gray-900">About</router-link>
                    <router-link to="/todo-app" class="mr-5 text-sm hover:text-gray-900">Todo App</router-link>
                </nav>
                <button class="inline-flex items-center bg-gray-100 border-0 py-1 px-3 leading-3 focus:outline-none hover:bg-gray-200 rounded text-sm font-bold mt-4 md:mt-0">Button
                    <svg fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" class="w-4 h-4 ml-1" viewBox="0 0 24 24">
                        <path d="M5 12h14M12 5l7 7-7 7"></path>
                    </svg>
                </button>
            </div>
        </header>
        <section class="py-10">
            <div class="container mx-auto">
                <router-view/>
            </div>
        </section>
    </div>
</template>

<style lang="scss">
    #app {
        font-family: 'Poppins', sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
</style>
