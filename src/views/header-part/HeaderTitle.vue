<template>
    <div class="header-title-container">
        <div class="header-title-left">
            <header-left-image/>
        </div>
        <div class="header-title-center">
            <a href="https://uzbekistan360.uz/ru/location/tv-tower"></a>
            <p>oculus</p>
        </div>
        <div class="header-title-right">
            <h1>VR</h1>
        </div>
    </div>
</template>
<script>
import HeaderLeftImage from './header-title-items/HeaderLeftImage.vue';
export default {
    name: 'sport-header',
    components: {HeaderLeftImage}
}
</script>