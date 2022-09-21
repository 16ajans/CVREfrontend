<script>
	let prefill;
</script>

<form>
	<fieldset>
		<legend>
			{#if !prefill}New{:else}Edit{/if} Player
		</legend>
		<label for="discord">Discord Tag</label>
		<input
			required
			type="text"
			id="discord"
			name="discord"
			value={prefill ? prefill.username + '#' + prefill.discriminator : ''}
		/>
		<label for="name">Name</label>
		<input required type="text" id="name" name="name" value={prefill ? prefill.name : ''} />
		<label for="school">School</label>
		<input required type="text" id="school" name="school" value={prefill ? prefill.school : ''} />
		<label for="verification">Enrollment Verification</label>
		<input required={!prefill} type="file" id="verification" name="verification" />
		<input type="reset" value="Cancel" />
		<input type="submit" value="Save" />
	</fieldset>
</form>
