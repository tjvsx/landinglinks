<script>
	//@ts-nocheck
	import { onMount } from 'svelte';
  import bg from '$lib/assets/bg.png'

	let canvas;

	onMount(() => {
		const ctx = canvas.getContext('2d');
		let frame = requestAnimationFrame(loop);

		function loop(t) {
			frame = requestAnimationFrame(loop);

			const imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);

			for (let p = 0; p < imageData.data.length; p += 4) {
				const i = p / 4;
				const x = i % canvas.width;
				const y = i / canvas.width >>> 0;

				const r =  (16 * x / canvas.width) + (8 * Math.sin(t / 1000));
				const g = (200 * y / canvas.height) + (32 * Math.cos(t / 1000));
				const b = 256;

				imageData.data[p + 0] = r;
				imageData.data[p + 1] = g;
				imageData.data[p + 2] = b;
				imageData.data[p + 3] = 255;
			}

			ctx.putImageData(imageData, 0, 0);
		}

		return () => {
			cancelAnimationFrame(frame);
		};
	});
</script>

<canvas
	bind:this={canvas}
	width={32}
	height={32}
/>
<div class='bg bg-l' />
<div class='bg bg-r' />
<div class='bg bg-main' />
<!-- <div class='bg bg-island' /> -->

<style>
	canvas {
		z-index: -1;
		position: absolute;
		width: 100%;
		height: 100%;
		opacity: 0.8;
		margin:0;
		left:0;
		right:0;
		bottom:0;
		top:0;
		padding:0;
		z-index: -2;
	}
	.bg {
		background-repeat: no-repeat;
		height: 18em;
		width: 18em;
		position: absolute;
		z-index: -1;
		/* dont scale */
		background-size: 100% auto;
		background-position: bottom;
	}
	.bg-l {
		background-image: url('$lib/assets/bg-l.png');
		left:0;
		bottom:0;
	}
	.bg-r {
		background-image: url('$lib/assets/bg-r.png');
		right:0;
		bottom:0;
	}
	.bg-main {
		background-image: url('$lib/assets/bg.png');
		background-repeat: no-repeat;
		background-size: 100% auto;
		height: 100%;
		background-position: bottom;
		opacity: 0.75;
		left:0;
		right:0;
		bottom:0;
		padding:0;
		z-index: -2;
		width: 100%;
	}

</style>