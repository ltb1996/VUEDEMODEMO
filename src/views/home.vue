<template>
    <div class="home-container"  v-if="showContent">
        <h1>Home Page</h1>
        <MobanYufa />
        <Shuxingbangding />
    </div>
</template>

<!-- 选项式api -->
<script>
import MobanYufa from '../components/mobanyufa.vue'
import Shuxingbangding from '../components/shuxingbangding.vue';

export default {
    name: 'Home',
    components: {
        MobanYufa,
        Shuxingbangding
    },
    data() {
        return {
            showContent: false
        }
    },
    mounted() {
        setTimeout(() => {
            this.showContent = true;
        }, 2000);
    }
}
</script>

<!-- 组合式api -->

<!-- <script setup>
import MobanYufa from '../components/mobanyufa.vue'
</script> -->

<style scoped>
.home-container {
    position: relative;
    z-index: 10;
}

h1 {
    z-index: 11;
    color: white;
}
</style>
