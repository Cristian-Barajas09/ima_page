<script lang="ts">
    import { menu } from "@store/global";
    import NavbarItem from "./NavbarItem.svelte";
    import MenuButton from '@components/layout/MenuButton.svelte'

    type Url = {
        name: string;
        url: string;
    }

    const urls: Array<Url> = [
        { name: "Inicio", url: "/" },
        { name: "Sobre nosotros", url: "/about" },
    ]
</script>

<div>
    <MenuButton/>
    <nav
        class="hidden md:flex lg:flex "
        class:active={$menu}
    >
        <ul
        class="flex flex-col md:flex-row lg:flex-row gap-2 w-full h-full mt-20 lg:m-0">
            {#each urls as {name, url} (url)}
                <NavbarItem name={name} url={url}/>
            {/each}
        </ul>
    </nav>
</div>

<style>
    .active {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 100vh;
        position: fixed;
        background-color: #fff;
        top: 0;
        left: 0;
        text-align: center;
        animation: fadeIn 0.5s;
        z-index: 10;
    }

    @keyframes fadeIn {
        from {
            opacity: 0;
        }
        to {
            opacity: 1;
        }
    }
</style>

