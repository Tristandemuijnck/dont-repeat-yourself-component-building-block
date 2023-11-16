<script>
    export let icon
</script>

<div class="icon">
    <img src="/images/icons/{icon}" alt="">
</div>

<style>
    .icon {
        width: var(--icon-width, 0.8rem);
        height: auto
    }

    img {
        width: 100%;
        height: 100%;
    }
</style>