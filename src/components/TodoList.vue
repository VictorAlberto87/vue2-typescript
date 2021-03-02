<template>
    <div>
        <todo-form @newTodo="newTodo($event)" />
        <div v-if="todos.length > 0" class="flex justify-end py-2">
            <button @click="removeTodos" class="inline-flex items-center bg-red-400 text-white border-0 py-3 px-4 leading-4 focus:outline-none rounded text-sm mt-4 md:mt-0">
                Eliminar Todos
            </button>
        </div>
        <table class="table-auto w-full text-left whitespace-no-wrap mt-6">
            <thead>
                <tr>
                    <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100 rounded-tl rounded-bl">id</th>
                    <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100">TODO</th>
                    <th class="px-4 py-3 title-font tracking-wider font-medium text-gray-900 text-sm bg-gray-100">Eliminar</th>
                </tr>
            </thead>
            <tbody v-if="todos.length > 0">
                <todo-item v-for="(todo, index) in todos" :todo="todo" :index="index" :key="index" @removeTodo="removeTodo(index)" />
            </tbody>
            <tbody v-else>
                <tr>
                    <td class="px-4 py-3 text-center" colspan="3">
                        <span class="text-sm font-normal text-gray-800">Agrega una tarea</span>
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from "vue-property-decorator";
    import TodoItem from "./TodoItem.vue";
    import TodoForm from "./TodoForm.vue";
    @Component({
        components: {
            TodoForm,
            TodoItem
        }
    })
    export default class TodoList extends Vue {
        todos: Array<string> = [];

        newTodo (todo: string) {
            this.todos.push(todo)
        }

        removeTodo (index: number) {
            this.todos.splice(index, 1)
        }
        removeTodos () {
            this.todos = []
        }
    }
</script>