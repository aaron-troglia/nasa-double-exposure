<script>
	export let compositeURL;

    let brightness = 50;
    let contrast = 100;
    let saturation = 25;

    const changeBrightness = (e) => {
        brightness = e.target.value;
    }

    const changeContrast = (e) => {
        contrast = e.target.value;
    }

    const changeSaturation = (e) => {
        saturation = e.target.value;
    }

    const exportImage = () => {
    }
</script>

{#if compositeURL}
	<div class="images-wrapper mx-auto my-8 shadow-2xl" id="double-exposure">
		<img src={compositeURL} class="composite-image text-center" width="500" height="500" id="composite" alt="Double Exposure" />
	</div>
{/if}


<style>
    .earth-image {
		width: 500px;
		height: 500px;
	}

	.user-image {
		position: absolute;
		top: 0;
		left: 0;
		width: 500px;
		height: 500px;
		mix-blend-mode: overlay;
		object-fit: cover;
		opacity: 1;
	}

	.images-wrapper {
		position: relative;
		width: 500px;
		height: auto;
	}

	.export {
	    display: inline-block;
	    padding: 0.5em 0.25em;
	    background-color: turquoise;
	    color: #fff;
	    border-radius: 5px;
	}
</style>
