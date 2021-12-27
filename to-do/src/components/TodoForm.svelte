<script type="ts">
   import { addTodo } from "../store/todoStore";
   let todo :any='';
   const handleSubit = () =>{
      addTodo(todo);
      todo = ''
   }
</script>

<form action="" on:submit|preventDefault={handleSubit} class="text-center flex items-center justify-center">
   <div class="flex items-center justify-center">
      <label for="todo" class="mr-5">Todo</label>
      <input type="text" bind:value={todo} name="todo" class="border border-cyan-700 rounded-md py-1 px-3" placeholder="Schedule your day">
      
   </div>
   <button type="submit" class="border border-cyan-300 py-1 px-3 rounded-lg hover:bg-cyan-700 hover:text-white mx-3">Submit</button>
</form>
