<script>
	import { onMount } from 'svelte';

    export let isDark = false;

    onMount(async () => {
        isDark = window.matchMedia("(prefers-color-scheme: dark)").matches;
        onThemeChange();
    });

    function onThemeChange(){
        document.querySelector(':root')
                .setAttribute('data-theme', isDark? 'dark':'light');
    }
</script>


<style>

</style>

<input 
    type="checkbox"
    class="switch"
    bind:checked={isDark}
    on:change={onThemeChange} />