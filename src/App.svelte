<script>
	import {onMount} from "svelte"

	let canvas

	onMount(()=> {
		
		const ctx = canvas.getContext('2d')
		
		ctx.fillRect(100, 100, 400, 20)

	})






</script>

<canvas bind:this={canvas} height={window.innerHeight} width={window.innerWidth}>
</canvas>

<style>

</style>