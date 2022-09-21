<script>
	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();

	function hide() {
		dispatch('hide');
	}

	let prefill;
</script>

<form>
	<fieldset>
		<legend>
			{#if !prefill}New{:else}Edit{/if} Team
		</legend>
		<label for="name">Name</label>
		<input required type="text" id="name" region="name" value={prefill ? prefill.name : ''} />
		<label for="region">Region</label>
		<input
			required
			type="text"
			id="region"
			region="region"
			list="regions"
			value={prefill ? prefill.region : ''}
		/>
		<datalist id="regions">
			<option value="Midwest" />
			<option value="Northeast" />
			<option value="Pacific" />
			<option value="Rocky Mountains" />
			<option value="Southeast" />
			<option value="Southwest" />
		</datalist>
		<label for="logo">Logo</label>
		<input type="file" id="logo" region="logo" />
		<input type="reset" value="Cancel" on:click={hide}/>
		<input type="submit" value="Save" />
	</fieldset>
</form>
