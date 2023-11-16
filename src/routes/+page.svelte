<script>
	import Button from '$lib/atoms/Button.svelte';
	import Icon from '$lib/atoms/Icon.svelte';
	import InputField from '$lib/atoms/InputField.svelte';
</script>

<!-- Button -->
<Button btnType="text" btnText="Inloggen"></Button>
<!-- <Button btnType="text" btnText="Inloggen" --btn-color="green"></Button> -->

<!-- Icon -->
<Icon iconSrc="/images/icons/arrow-right.svg" --icon-width="1.6rem"></Icon>

<!-- InputField -->
<InputField inputType="text" inputPlaceholder="Vul hier uw emailadres in" inputName="email" inputId="email"></InputField>
