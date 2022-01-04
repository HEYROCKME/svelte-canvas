<script>
	import {onMount} from "svelte"

	let canvas
	let resVal = 5

	onMount(()=> {
		
		const ctx = canvas.getContext('2d')
		const image1 = new Image()
		image1.src="../img/ALWN1427.JPG"
		image1.width = 500
		image1.height = 500
		image1.onload = function init() {
			canvas.width = image1.width
			canvas.height = image1.height
			ctx.drawImage(image1, 0, 0)

		}
		
	
		// // let positionX = 100
		
		// // for( let i = 1; i<10; i++ ) {
		// // 	let x = positionX
		// // 	let y = 20 * i * i / 5
		// // 	let width = 50 * i
		// // 	let positionY = i * 4

		// // 	ctx.fillRect(x, y, width, positionY)

		// }
		
		

	})






</script>

<canvas bind:this={canvas} height={window.innerHeight* 0.75} width={window.innerWidth * 0.75}>
</canvas>

<div class="controls">
	<label for="resolution">Resolution: {resVal}</label>
	<input bind:value={resVal} type="range" name="resolution" id="resolution" min="1" max="20">
</div>

<style>
	

canvas {
	background-color: salmon;
}
</style>