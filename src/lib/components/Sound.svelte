<script>
	import Block from './Block.svelte';

	const style = 'm-0 p-0 absolute top-6 text-white';
	const stroke = '#BD42BD';
	const fill = '#CF63CF';
</script>

<div class="relative w-80 text-while p-0 m-0">
	<p class="{style} left-4">start sound</p>
	<button class="{style} p-0 m-0 rounded-full right-24 border border-[#BD42BD] bg-[#C94FC9] px-2"
		>costume1</button
	>
	<Block {fill} {stroke} width="220" />
</div>
