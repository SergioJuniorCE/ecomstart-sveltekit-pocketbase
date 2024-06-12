<script lang="ts">
	import * as Sheet from '$lib/components/ui/sheet';
	import Menu from 'lucide-svelte/icons/menu';
	import { onMount } from 'svelte';

	let categories: {
		title: string;
		slug: string;
	}[];

	onMount(() => {
		categories = [
			{
				title: 'Home',
				slug: ''
			},
			{
				title: 'About',
				slug: 'about'
			},
			{
				title: 'Contact',
				slug: 'contact'
			},
			{
				title: 'Blog',
				slug: 'blog'
			}
		];
	});
</script>

<Sheet.Root>
	<Sheet.Trigger>
		<Menu />
	</Sheet.Trigger>
	<Sheet.Content>
		<nav class="flex flex-col place-items-end gap-4">
			{#each categories as category}
				<a href="/{category.slug}" class="text-gray-600 hover:text-gray-900">
					{category.title}
				</a>
			{/each}
		</nav>
	</Sheet.Content>
</Sheet.Root>
