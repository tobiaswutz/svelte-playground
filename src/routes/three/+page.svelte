<script lang="ts">
	import { Canvas, InteractiveObject, OrbitControls, T } from '@threlte/core';
	import { spring } from 'svelte/motion';
	import { degToRad } from 'three/src/math/MathUtils';

	const scale = spring(1);
</script>

<div>
	<Canvas>
		<T.PerspectiveCamera makeDefault position={[10, 10, 10]} fov={24}>
			<OrbitControls
				autoRotate
				enableZoom={true}
				target={{ y: 0.5 }}
			/>
		</T.PerspectiveCamera>

		<T.DirectionalLight castShadow position={[3, 10, 10]} />
		<T.DirectionalLight position={[-3, 10, -10]} intensity={0.2} />
		<T.AmbientLight intensity={0.2} />

		<!-- Cube -->
		<T.Group scale={$scale}>
			<T.Mesh position.y={0.5} castShadow let:ref>
				<!-- Add interaction -->
				<InteractiveObject
					object={ref}
					interactive
				/>

				<T.BoxGeometry />
				<T.MeshStandardMaterial color="blue" />
			</T.Mesh>
		</T.Group>
	</Canvas>
</div>

<style>
	div {
		height: 100vh;
		width: 100%;
	}

    canvas {
        height: 100%;
        width: 100%;
    }
</style>
