<script lang="ts">
	let active: boolean = false;
	import Button from "$lib/components/Button.svelte";
	import Dropmenu from "$lib/components/Dropmenu.svelte";


	const toggleActieve = () => {
		active = !active;
		console.log('Hallo mein Name ist Tobias ich habe gerade diesesn Butten gehovert!')
	};
</script>

<div class="h-screen text-white bg-gray-900">
	<div>
		<div class="p-10 h-screen w-full">
				<Dropmenu />

			<!-- <div class="h-full w-full border-2 border-orange-400 flex justify-center items-center">
				<Button on:click={toggleActieve}>Hallo ich</Button>
				<Dropmenu />
			</div> -->
		</div>
	</div>
</div>

<style>
	.active {
		background-color: red;
	}
</style>
