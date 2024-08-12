<script lang="ts">
    import HamburguerIcon from '../icons/HamburguerIcon.svelte';
    import XIcon from '../icons/XIcon.svelte';
    
    import { menu } from '@store/global.ts'

    const handleClick = () => {
        menu.update((value) => !value)
    }

    $: showButton = $menu ? "fixed top-2 right-2 z-50" : ""

</script>

<button
    class={`w-12 md:hidden lg:hidden  ${showButton}`}
    on:click={handleClick}
>
    {#if $menu}
        <XIcon className="w-full h-full"/>
    {:else}
        <HamburguerIcon className="w-full h-full"/>
    {/if}
</button>

