<template>
    <div>
        <div class="flex flex-col text-center w-full mb-12">
            <h1 class="sm:text-3xl text-2xl font-medium title-font mb-4 text-gray-900">Create Todo</h1>
            <p class="lg:w-2/3 mx-auto leading-relaxed text-base">Whatever cardigan tote bag tumblr hexagon brooklyn asymmetrical gentrify.</p>
        </div>
        <form @submit.prevent="addTodo">
            <div class="lg:w-1/2 md:w-2/3 mx-auto">
                <div class="flex items-end -m-2">
                    <div class="p-2 flex-1">
                        <div class="relative">
                            <label for="todo" class="leading-7 text-sm font-bold text-left text-gray-600 block">Todo:</label>
                            <input v-model="todo" autocomplete="off" type="text" id="todo" name="todo" class="w-full bg-gray-100 bg-opacity-50 rounded border border-gray-300 focus:border-indigo-500 focus:bg-white focus:ring-2 focus:ring-indigo-200 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out">
                        </div>
                    </div>
                    <div class="p-2 flex-shrink-0">
                        <button type="submit" class="flex mx-auto text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg">Agregar todo</button>
                    </div>
                </div>
            </div>
        </form>
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from "vue-property-decorator";
    @Component
    export default class TodoForm extends Vue {
        todo: String = ''
        addTodo () {
            this.$emit('newTodo', this.todo)
            this.todo = ''
        }
    }
</script>