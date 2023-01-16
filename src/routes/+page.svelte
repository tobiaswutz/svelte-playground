<script lang="ts">
	let active: boolean = false;
	import Dropmenu from '$lib/components/Dropmenu.svelte';

	let choices: any[] = [
		'test1',
		'test2',
		'test3',
		'test4',
		'test5',
		'test6',
		'test7',
		'test8',
		'test9',
		'test10'
	];
	let current: any = null;
</script>

<div class="h-screen text-white bg-gray-900">
	<div>
		<div class="p-10 h-screen w-full">
			<Dropmenu bind:current {choices} />
		</div>
	</div>
</div>

<style>
	.active {
		background-color: red;
	}
</style>
