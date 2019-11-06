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
	.center {
	  text-align: center;
	}

	.pagination {
	  display: inline-block;
	}

	.pagination-control {
	  color: black;
	  float: left;
	  padding: 8px 16px;
	  text-decoration: none;
	  transition: background-color .3s;
	}

	.pagination-control.active {
	  background-color: #990000;
	  color: white;
	  border: 1px solid #990000;
	}

	.pagination span:hover:not(.active) {
		background-color: #ddd;
	}

	.pager {	
		width: 600px;
		position: relative;
		margin: auto;
	}
	
	.page-content {
		height: 400px;
		position: absolute;
		overflow: auto;
	}

	.page-number {
		margin: auto;
	}
</style>

<div class="pager">	
	<div class="center">
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
	</div>

	<div class="page" >
		{#each contents as page(page.id)}
		{#if index == page.id}
		<div class="page-content" transition:fade>
			{@html page.content}
		</div>
		{/if}
		{/each}
	</div>

</div>