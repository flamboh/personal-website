<script lang="ts">
	export let title: string;
	export let id: string = title.toLowerCase().replace(/\s+/g, '-');
</script>

<section class="mb-8" {id}>
	<h2 class="mb-4 border-b border-gray-300 pb-2 text-2xl font-semibold">{title}</h2>
	<div>
		<slot />
	</div>
</section>
