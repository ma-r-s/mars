<script>
	import { T } from '@threlte/core';
	import { OrbitControls } from '@threlte/extras';
</script>

<T.PerspectiveCamera makeDefault position={[1, 1, 0]}>
	<OrbitControls enablePan={false} enableZoom enableDamping autoRotate />
</T.PerspectiveCamera>
<T.Mesh position.y={-0.5}>
	<T.SphereGeometry args={[1, 16, 16]} />
	<T.MeshBasicMaterial wireframe />
</T.Mesh>
