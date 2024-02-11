<script lang="ts">
	import Editor from '$lib/components/Editor.svelte';
	import MentionComponent from '$lib/components/MentionComponent.svelte';

	let content = '';
	let names = ['nick'];
</script>

<div class="flex h-full w-full">
	<!-- sidebar -->
	<div class="h-full basis-1/4 border-r border-r-black"></div>
	<!-- main content -->
	<div class="h-full basis-3/4">
		<Editor
			bind:content
			keywordMap={{
				'@': {
					component: MentionComponent,
					recognized: names,
					allowUnrecognized: false
				}
			}}
		/>
	</div>
</div>
