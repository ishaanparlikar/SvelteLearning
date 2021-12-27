<script>
	import { deleteTodo, toggleState } from '../store/todoStore';
	export let todo;
	export let index;
</script>

<li
	class={`flex items-center justify-between p-4 shadow-sm border border-cyan-300 rounded-md mx-auto ${
		todo.completed ? 'bg-cyan-200' : ''
	}`}
>
	<input
		type="checkbox"
		name="completed"
		checked={todo.completed}
		on:change={() => toggleState(todo.id)}
		id=""
	/>
	<h3 class={`text-lg text-bold ${todo.completed ? 'line-through' : ''}`}>{todo.text}</h3>
	<button
		on:click={() => deleteTodo(todo.id)}
		class="border border-red-300 py-1 px-3 rounded-lg hover:bg-red-700 hover:text-white mx-3"
		>Delete</button
	>
</li>
