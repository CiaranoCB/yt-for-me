<script lang="ts">
	import gsap from 'gsap';

	export let thumbnail = '';
	export let title = '';
	export let creator = '';
	export let views = '';
	export let avatar = '';
	export let loading = true;
	export let id = 0;

	function hover() {
        setTimeout(() => {

        
		    gsap.to('.thumbnail-' + id, {
			    scale: 1.2,
			    duration: 0.5
		    });
        });
	}

	function out() {
		gsap.to('.thumbnail-' + id, {
			scale: 1,
			duration: 0.5
		});
	}

	$: classes = 'thumbnail-' + id;
</script>

<section>
	<a class="bind:thumbnail bg-slate-600 m-4" 
    href="/" 
    on:mouseover={hover} 
    on:focus={hover} 
    on:mouseout={out} 
    on:blur={out}>
		{#if !loading}
			<img class={classes} src={thumbnail} alt="" />
		{/if}
	</a>
	<div class="flex gap-4 mx-4">
		<div class="avatar bg-slate-600">
			{#if !loading}
				<img src={avatar} alt="" />
			{/if}
		</div>
		<div>
			{#if !loading}
				<div class="long-text mb-4">{title}</div>
				<div class="text">{creator} | {views}</div>
			{:else}
				<div class="long-text bg-slate-600 mb-4" />
				<div class="text bg-slate-600" />
			{/if}
		</div>
	</div>
</section>

<style>
	.thumbnail {
		width: 320px;
		height: 180px;
	}

	.avatar {
		width: 30px;
		height: 30px;
		border-radius: 50%;
	}

	.long-text {
		width: 230px;
		height: 20px;
	}

	.text {
		width: 200px;
		height: 20px;
	}
</style>
