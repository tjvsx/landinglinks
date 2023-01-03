<div class='fg fg-l' />
<div class='fg fg-r' />
<div class='fg fg-l1' />
<div class='fg fg-r1' />


<style>
  .fg {
		background-repeat: no-repeat;
    display: flex;
		position: absolute;
		z-index: 1;
    height: 15em;
    width: 15em;
		/* dont scale */
		background-size: 100% auto;
		background-position: top;
	}
	.fg-r {
		background-image: url('$lib/assets/fg-r.png');
		right:0;
		top:0;
	}
  .fg-l {
    background-image: url('$lib/assets/fg-l.png');
    left:0;
    top:0;
  }

</style>