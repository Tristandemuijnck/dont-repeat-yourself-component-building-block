<script>
	import { applyAction, enhance } from '$app/forms'

	import FormField from '$lib/molecules/FormField.svelte'
	import Button from '$lib/atoms/Button.svelte'

	export let formAction
	export let formMethod
    export let btnText

	let loading = false

	const handleSubmit = () => {
		loading = true
		return async ({ result }) => {
			await applyAction(result)
			loading = false
		}
	}
</script>

<form action={formAction} method={formMethod} use:enhance={handleSubmit}>
	<div class="form-content">
		<FormField
			iconSrc="/images/icons/email.svg"
			labelFor="email"
			labelText="Emailadres"
			inputType="text"
			inputPlaceholder="Vul hier uw emailadres in"
			inputName="email"
			inputId="email"
		></FormField>
	</div>

	<Button btnType="submit" {btnText}></Button>
</form>

<style>
	form {
		display: flex;
		flex-direction: column;
		row-gap: 2rem;
		width: auto;
	}

	.form-content {
		display: flex;
		flex-direction: column;
		padding: 2rem;
		background: var(--form-bg, #1e1649);
	}
</style>
