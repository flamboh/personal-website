<script lang="ts">
	import pfp from '$lib/assets/pfp.jpeg';
	export let title: string = 'Infobox Title';
	export let items: { label: string; value: string }[] = [];
</script>

<div class="float-right mb-6 w-64 border border-gray-300 bg-gray-100 p-4 text-sm">
	<h2 class="mb-2 text-center text-lg font-semibold">{title}</h2>
	{#if items.length > 0}
		<img src={pfp} alt={title} class="mb-4 w-full rounded-sm" />
		<div class="mb-4 text-center">
			<a
				href="/resume.pdf"
				class="text-blue-600 hover:underline"
				target="_blank"
				rel="noopener noreferrer"
			>
				Resume
			</a>
		</div>

		<table class="w-full">
			<tbody>
				{#each items as item}
					<tr class="border-t border-gray-300">
						<th class="py-1 pr-2 text-left align-top">{item.label}</th>
						<td class="py-1">
							{#if item.value.startsWith('http://') || item.value.startsWith('https://') || item.value.includes('.com') || item.value.includes('.wiki')}
								<a
									href={item.value.startsWith('http') ? item.value : `https://${item.value}`}
									class="text-blue-600 hover:underline"
									target="_blank"
									rel="noopener noreferrer">{item.value}</a
								>
							{:else if item.value.includes('@')}
								<a href={`mailto:${item.value}`} class="text-blue-600 hover:underline"
									>{item.value}</a
								>
							{:else}
								{item.value}
							{/if}
						</td>
					</tr>
				{/each}
			</tbody>
		</table>
	{/if}
	<slot />
</div>
