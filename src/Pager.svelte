<script>
	import { fade } from 'svelte/transition';
	export let contents = [];
	let index = 0;
	
	function handleNext() {
		index = index + 1;
	}
	
	function handlePrev() {
		index = index - 1;
	}
</script>

<style>
	.pagination {
	  display: flex;
	  justify-content: center;
	  flex-direction: row;
	}

	.pagination-control {
	  color: black;
	  margin: 0 0 0.5em 0;
	  padding: 0.5em 1em;
	  transition: background-color .3s;
	}

	.pagination-control.active {
	  background-color: #990000;
	  color: white;
	}

	.pagination span:hover:not(.active) {
		background-color: #ddd;
	}

	.pager {	
		position: relative;
		margin: auto;
		display: flex;
		flex-direction: column	
	}

	.page-content {
		left: 0;
		right: 0;
		position: absolute;
		margin: auto;
		overflow: auto;
	}

	@media screen and (min-width: 864px) {
	  .page-content {
		max-width: 80vw;
	  }
	}


</style>

<div class="pager">	
		<div class="pagination">
			<button class="pagination-control"
				on:click="{() => index -=1}" 
				disabled="{index == 0}">
				&lt;
			</button>
			{#each contents as page(page.id)}
				<span class="pagination-control {index === page.id ? 'active' : ''}"
					  on:click="{() => index = page.id}"
				>{page.id + 1}</span>
			{/each}
			<button class="pagination-control"
				on:click="{() => index +=1}"
				disabled="{index == contents.length - 1}">
				&gt;
			</button>
		</div>
	
		<div>
			{#each contents as page(page.id)}
			{#if index == page.id}
			<div class="page-content" transition:fade>
				{@html page.content}
			</div>
			{/if}
			{/each}
		</div>

</div>