<template>
    <div class="main-dashboard-layout">
        <dashboard-header/>
        <dashboard-content/>
        <dashboard-footer/>
    </div>
</template>
<script>
import DashboardHeader from './DashboardHeader.vue';
import DashboardContent from './DashboardContent.vue';
import DashboardFooter from './DashboardFooter.vue';
export default {
    name: 'dashboard-layout',
    components: {DashboardHeader, DashboardContent, DashboardFooter}
}
</script>