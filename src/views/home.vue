<!--
 * @Author: ltb1996 610030835@qq.com
 * @Date: 2025-10-04 19:55:28
 * @LastEditors: ltb1996 610030835@qq.com
 * @LastEditTime: 2025-11-02 00:04:20
 * @FilePath: \vuedemodemo\src\views\home.vue
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
<template>
    <div class="home-container" v-if="showContent">
        <h1>Home Page vue3官网教学</h1>
        <hr>
        <MobanYufa />
        <Shuxingbangding />
        <Tiaojianxuanran />
        <Libiaoxuanran />
        <Keyguanlizhuangtai />
        <Shijianchuli />
        <Shijianchuancan />
        <Eventdemo />
        <Shijianxiushifu></Shijianxiushifu>
        <Shuzubianhuazhence />
        <Jisuanshuxing />
        <Classbangding />
        <Stylebangding />
        <Wacthczhenting />
        <Biaodanshujubangding />
        <Mobanyinyong />
    </div>
</template>

<!-- 选项式api -->
<script>
import MobanYufa from '../components/mobanyufa.vue'
import Shuxingbangding from '../components/shuxingbangding.vue';
import Tiaojianxuanran from '../components/tiaojianxuanran.vue';
import Libiaoxuanran from '../components/libiaoxuanran.vue';
import Keyguanlizhuangtai from '../components/keyguanlizhuangtai.vue';
import Shijianchuli from '../components/shijianchuli.vue';
import Shijianchuancan from '../components/shijianchuancan.vue';
import Eventdemo from '../components/eventdemo.vue';
import Shijianxiushifu from '../components/shijianxiushifu.vue';
import Shuzubianhuazhence from '../components/shuzubianhuazhence.vue';
import Jisuanshuxing from '../components/jisuanshuxing.vue';
import Classbangding from '../components/classbangding.vue';
import Stylebangding from '../components/stylebangding.vue';
import Wacthczhenting from '../components/wacthczhenting.vue';
import Biaodanshujubangding from '../components/biaodanshujubangding.vue';
import Mobanyinyong from '../components/mobanyinyong.vue';


export default {
    name: 'Home',
    components: {
        MobanYufa,
        Shuxingbangding,
        Tiaojianxuanran,
        Libiaoxuanran,
        Keyguanlizhuangtai,
        Shijianchuli,
        Shijianchuancan,
        Eventdemo,
        Shijianxiushifu,
        Shuzubianhuazhence,
        Jisuanshuxing,
        Classbangding,
        Stylebangding,
        Wacthczhenting,
        Biaodanshujubangding,
        Mobanyinyong
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
