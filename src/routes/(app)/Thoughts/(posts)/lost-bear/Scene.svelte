<script>
	import { T } from '@threlte/core';
	import { OrbitControls, GLTF } from '@threlte/extras';
	import { interactivity } from '@threlte/extras';
	interactivity();
</script>

<T.PerspectiveCamera look makeDefault position={[-0.5, 0.5, 1.5]}>
	<OrbitControls enablePan={false} enableZoom enableDamping />
</T.PerspectiveCamera>
<T.AmbientLight intensity={3} />
<GLTF url={'/3D/bear/scene.gltf'} scale={0.1} position={[-0.76, 0.26, 0]} rotation={[0, 0, 0.8]}
></GLTF>
<T.Mesh position.y={-0.5}>
	<T.SphereGeometry args={[1, 32, 32]} />
	<T.MeshNormalMaterial wireframe />
</T.Mesh>
<T.Mesh position.y={0.5}>
	<T.SphereGeometry args={[0.03, 16, 16]} />
	<T.MeshStandardMaterial color="red" />
</T.Mesh>
<T.Mesh position.y={-1.5}>
	<T.SphereGeometry args={[0.03, 16, 16]} />
	<T.MeshStandardMaterial color="blue" />
</T.Mesh>
