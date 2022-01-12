<template>
    <div id="tasks">
        <form v-on:submit.prevent="addNewTodo">
            <label for="new-todo">Add a todo</label>
            <input v-model="newTodoText"
            id="new-todo"
            placeholder="E.g. feed the cat">
            <button>Add</button>
        </form>
        <ul>
            <li is="todo-item"
            v-for="(todo, index) in todos"
            v-bind:key="todo.id"
            v-bind:title="todo.title"
            v-on:remove="todos.splice(index, 1)"></li>
        </ul>
    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component
    export default class Tasks extends Vue {
        @Prop() title!: string
        
    }

    new Vue({
        el: '#tasks',
        data: {
            newTodoText: '',
            todos: [
                {
                    id: 1,
                    title: 'do something'
                },
                {
                    id: 2,
                    title: 'do something else'
                }, 
                {
                    id: 3,
                    title: 'maw the lawn'
                }
            ],
            nextTodoId: 4
        },
        methods: {
            addNewTodo: function () {
                this.todos.push({
                    id: this.nextTodoId++,
                    title: this.newTodoText
                })
                this.newTodoText = ''
            }
        }
    })
</script>
