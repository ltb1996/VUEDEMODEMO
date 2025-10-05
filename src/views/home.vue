<template>
    <div class="home-container"  v-if="showContent">
        <h1>Home Page vue3官网教学</h1>
        <MobanYufa />
        <Shuxingbangding />
        <Tiaojianxuanran />
        <Libiaoxuanran />
        <Keyguanlizhuangtai />
    </div>
</template>

<!-- 选项式api -->
<script>
import MobanYufa from '../components/mobanyufa.vue'
import Shuxingbangding from '../components/shuxingbangding.vue';
import Tiaojianxuanran from '../components/tiaojianxuanran.vue';
import Libiaoxuanran from '../components/libiaoxuanran.vue';
import Keyguanlizhuangtai from '../components/keyguanlizhuangtai.vue';


export default {
    name: 'Home',
    components: {
        MobanYufa,
        Shuxingbangding,
        Tiaojianxuanran,
        Libiaoxuanran,
        Keyguanlizhuangtai
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
