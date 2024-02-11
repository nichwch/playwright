<script lang="ts">
	import Editor from '$lib/components/Editor.svelte';
	import MentionComponent from '$lib/components/MentionComponent.svelte';

	let content = '';
	let names = ['nick'];
</script>

<div class=" box-border flex h-screen w-full overflow-y-hidden p-10">
	<!-- sidebar -->
	<div class=" h-full basis-1/4 border-r border-r-black"></div>
	<!-- main content -->
	<div class=" flex h-full basis-3/4 flex-col p-10">
		<!-- editor -->
		<div class="basis-1/2">
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
		<div class="basis-1/2 border border-black">hello</div>
	</div>
</div>
