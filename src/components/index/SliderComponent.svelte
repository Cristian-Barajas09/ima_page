<script lang="ts">
    import { images } from '@data/gallery.json';
    import Carousel from './Carousel.svelte';
</script>

<Carousel>
    <img
        src="{images[0].src}"
        alt="{images[0].title}"
    />
</Carousel>