<script lang="ts">
	let active: boolean = false;

	const toggleActieve = () => {
		active = !active;
	};
</script>

<div class="h-screen text-white bg-gray-900">
	<div>
		<div class="p-10 h-screen w-full">
			<div class="h-full w-full border-2 border-orange-400 flex justify-center items-center">
				<button
					on:click={toggleActieve}
					class="p-2 rounded-lg border-2 border-green-400"
					class:active={active}>ICH BIN EIN BUTTON!</button
				>
			</div>
		</div>
	</div>
</div>

<style>
	.active {
		background-color: red;
	}
</style>
