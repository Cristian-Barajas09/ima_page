<script lang="ts">
  import { menu } from "@store/global";
  import { navigate } from "astro:transitions/client";

    export let name: string;
    export let url: string;

    const handleClick = (path: string) => {
        menu.set(false);
        navigate(path);
    }

</script>

<li class="hover:border-b-2 transition-all duration-200">
    <button
        class="p-2 w-full"
        on:click={() => handleClick(url)}
    >
        {name}
    </button>
</li>