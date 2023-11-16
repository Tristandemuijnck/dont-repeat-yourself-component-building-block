<script>
	import Button from '$lib/atoms/Button.svelte'
	import Icon from '$lib/atoms/Icon.svelte'
	import InputField from '$lib/atoms/InputField.svelte'
	import Label from '$lib/atoms/Label.svelte'

	import FormField from '../lib/molecules/FormField.svelte'
</script>

<!-- Atoms -->
<div class="atoms">
	<!-- Button -->
	<Button
        btnType="text"
        btnText="Inloggen"
    ></Button>
	<!-- <Button btnType="text" btnText="Inloggen" --btn-color="green"></Button> -->

	<!-- Icon -->
	<Icon
        iconSrc="/images/icons/arrow-right.svg"
        --icon-width="1.6rem"
    ></Icon>

	<!-- InputField -->
	<InputField
		inputType="text"
		inputPlaceholder="Vul hier uw emailadres in"
		inputName="email"
		inputId="email"
	></InputField>

	<!-- Label -->
	<Label
        labelFor="email"
        labelText="Emailadres"
    ></Label>
</div>

<!-- Molecules -->
<div class="molecules">
	<!-- FormField -->
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

<style>
	.atoms {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		width: 12rem;
		margin: 5rem;
	}
</style>
