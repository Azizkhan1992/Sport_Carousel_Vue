<template>
    <div class="dashboard-header-container">
        <div class="dashboard-header-content">
            <header-title/>
            <header-sidebar/>
        </div>

    </div>
</template>
<script>
import HeaderTitle from '@/views/header-part/HeaderTitle.vue';
import HeaderSidebar from '@/views/header-part/HeaderSidebar.vue';
export default {
    name: 'dashboard-header',
    components: {HeaderTitle, HeaderSidebar}
}
</script>