<script>
	import { prompt } from '$lib/stores';
	const style = 'm-0 p-0 absolute top-6 text-white';
	const stroke = '#774DCB';
	const fill = '#855CD6';
	import Block from './Block.svelte';

	export let type = 'costume'; // or 'backdrop'
</script>

{#if type === 'costume'}
	<div class="relative w-80 text-while">
		<p class="{style} left-4">switch costume to</p>
		<button class="{style} rounded-full right-16 border border-[#774DCB] bg-[#855CD6] px-2"
			>costume1</button
		>
		<Block {fill} {stroke} width="260" />
	</div>
{:else if type === 'backdrop'}
	<div class="relative w-80 text-while">
		<p class="{style} left-4">switch backdrop to</p>
		<button class="{style} rounded-full right-4 border border-[#774DCB] bg-[#855CD6] px-2"
			>backdrop1</button
		>
		<Block {fill} {stroke} width="300" />
	</div>
{:else if type === 'say'}
	<div class="relative w-80 text-while">
		<p class="{style} left-4">say</p>
		<input
			bind:value={$prompt}
			class="m-0 p-0 absolute top-6 left-16 text-gray-600 px-1 rounded-full"
			type="text"
			maxlength="65"
			placeholder="... something"
		/>
		<Block {fill} {stroke} width="300" />
	</div>
{/if}
