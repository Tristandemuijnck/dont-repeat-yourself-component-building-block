<script>
	import Button from '$lib/atoms/Button.svelte'
	import Icon from '$lib/atoms/Icon.svelte'
	import InputField from '$lib/atoms/InputField.svelte'
	import Label from '$lib/atoms/Label.svelte'

	import FormField from '$lib/molecules/FormField.svelte'

    import LoginForm from '$lib/organisms/LoginForm.svelte'
</script>

<main>
	<h1>Login Form Atomic Design</h1>

	<!-- Atoms -->
	<section class="atoms">
		<h2>Atoms</h2>

		<div class="atom-field">
			<h3>Button:</h3>
			<!-- Button -->
			<Button btnType="text" btnText="Inloggen"></Button>
			<!-- <Button btnType="text" btnText="Inloggen" --btn-color="green"></Button> -->
		</div>

		<div class="atom-field">
			<h3>Icon:</h3>
			<!-- Icon -->
			<Icon iconSrc="/images/icons/arrow-right.svg" --icon-width="1.6rem"></Icon>
		</div>

		<div class="atom-field">
			<h3>Input Field:</h3>
			<!-- InputField -->
			<InputField
				inputType="text"
				inputPlaceholder="Vul hier uw emailadres in"
				inputName="email"
				inputId="email"
			></InputField>
		</div>

		<div class="atom-field">
			<h3>Label:</h3>
			<!-- Label -->
			<Label labelFor="email" labelText="Emailadres"></Label>
		</div>
	</section>

	<!-- Molecules -->
	<section class="molecules">
		<h2>Molecules</h2>

		<div class="molecule-field">
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
	</section>

    <!-- Organisms -->
    <section class="organisms">
        <h2>Organisms</h2>

        <div class="organism-field">
            <!-- LoginForm -->
            <LoginForm formAction="" formMethod="POST" btnText="Inloggen"></LoginForm>
        </div>
    </section>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: left;
	}

	h1 {
		margin-top: 5rem;
	}

	.atoms {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		width: auto;
		margin-top: 2rem;
        padding: 0 1rem;
	}

	.atom-field {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
		background-color: rgba(255, 255, 255, 0.405);
		padding: 1rem;
		border-radius: 0.5rem;
		margin-left: 1rem;
        max-width: 20rem;
	}

	.molecules {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		width: auto;
		margin-top: 2rem;
        padding: 0 1rem;
	}

	.molecule-field {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
		background-color: rgba(255, 255, 255, 0.405);
		padding: 1rem;
		border-radius: 0.5rem;
		margin-left: 1rem;
        max-width: 20rem;
	}

    .organisms {
        display: flex;
		flex-direction: column;
		gap: 1rem;
		width: auto;
		margin-top: 2rem;
        margin-bottom: 4rem;
        padding: 0 1rem;
    }

    .organism-field {
        display: flex;
		flex-direction: column;
		gap: 0.8rem;
		background-color: rgba(255, 255, 255, 0.405);
		padding: 1rem;
		border-radius: 0.5rem;
		margin-left: 1rem;
        max-width: 20rem;
    }

	@media (min-width: 425px) {
		main {
			align-items: unset;
		}

        h1{
            margin: 4rem 1rem 0 2rem;
        }

        .atoms{
            margin-left: 2rem;
        }

        .molecules{
            margin-left: 2rem;
        }

        .organisms{
            margin-left: 2rem;
            width: 25rem;
        }
	}

    @media (min-width: 768px) {
        h1{
            margin: 4rem 1rem 0 4rem;
        }

        .atoms{
            margin-left: 4rem;
        }

        .molecules{
            margin-left: 4rem;
        }

        .organisms{
            margin-left: 4rem;
        }
	}

    @media (min-width: 1024px) {
        h1{
            margin: 4rem 1rem 0 6rem;
        }

        .atoms{
            margin-left: 6rem;
        }

        .molecules{
            margin-left: 6rem;
        }

        .organisms{
            margin-left: 6rem;
        }
	}
</style>
