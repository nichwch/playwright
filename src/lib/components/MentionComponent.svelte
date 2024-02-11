<button
	on:click={() => {
		window.alert('hello');
	}}
	class="border-box block border border-blue-700 bg-blue-200 text-blue-700 hover:bg-blue-300"
>
	<slot />
</button>
