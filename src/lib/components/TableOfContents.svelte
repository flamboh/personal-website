<script lang="ts">
	export let sections: { title: string; id: string }[] = [];
</script>

<div class="mb-6 w-fit max-w-md border border-gray-300 bg-gray-50 p-4">
	<h2 class="mb-2 text-lg font-bold">Contents</h2>
	{#if sections.length > 0}
		<ol class="ml-4 list-inside list-decimal space-y-1">
			{#each sections as section, i}
				<li>
					<a href="#{section.id}" class="text-blue-600 hover:underline">{section.title}</a>
				</li>
			{/each}
		</ol>
	{:else}
		<p class="text-sm text-gray-500">No sections defined yet.</p>
	{/if}
</div>
