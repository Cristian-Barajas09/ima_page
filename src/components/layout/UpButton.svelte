<script lang="ts">
  import ArrowUpIcon from "@components/icons/ArrowUpIcon.svelte";

    const handleClickButton = () => {
        const navbar = document.getElementById('navbar') as HTMLElementTagNameMap["nav"];

        navbar.scrollIntoView({ behavior: 'smooth' });

    }
</script>


<button
    on:click={handleClickButton}
    class="bg-[#333] p-2 rounded shadow-zinc-600 shadow-xl fixed z-10 bottom-2 right-2"
>
    <ArrowUpIcon className="text-white"/>
</button>