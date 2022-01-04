<script>
	import {onMount} from "svelte"

	let canvas

	onMount(()=> {
		
		const ctx = canvas.getContext('2d')
		
		let positionX = 100
		
		for( let i = 1; i<10; i++ ) {
			let x = positionX
			let y = 20 * i * i / 5
			let width = 50 * i
			let positionY = i * 4

			ctx.fillRect(x, y, width, positionY)

		}
		
		

	})






</script>

<canvas bind:this={canvas} height={window.innerHeight* 0.5} width={window.innerWidth * 0.5}>
</canvas>

<div class="controls">
	<input type="range" name="resolution" id="resolution" min="1" max="20">
</div>

<style>

</style>