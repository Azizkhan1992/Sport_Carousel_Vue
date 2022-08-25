<template>
    <div class="carousel-container">
        <content-carousel/>
    </div>
</template>
<script>
import ContentCarousel from '@/views/content/ContentCarousel.vue';
export default {
    name: 'carousel-content',
    components:{ContentCarousel}
}
</script>