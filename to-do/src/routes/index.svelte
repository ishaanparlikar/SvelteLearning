<script lang="ts">
	import { each } from 'svelte/internal';

	import TodoForm from '../components/TodoForm.svelte';
	import { todos } from '../store/todoStore';
	import Todo from '../components/Todo.svelte';
</script>

<main>
	<h1 class="text-center text-2xl mb-5">To Dos</h1>
	<TodoForm />
	<ul class="my-5 w-96 mx-auto">
		{#each $todos as todo}
			<Todo {todo} index={todo.id} />
		{/each}
	</ul>
</main>
