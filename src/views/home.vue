<template>
    <div>
        <h1>Home Page</h1>
        <MobanYufa />
    </div>
</template>

<!-- 选项式api -->
<script>
import MobanYufa from '../components/mobanyufa.vue'

export default {
    name: 'Home',
    components: {
        MobanYufa
    }
}
</script>

<!-- 组合式api -->

<!-- <script setup>
import MobanYufa from '../components/mobanyufa.vue'
</script> -->

<style scoped></style>
