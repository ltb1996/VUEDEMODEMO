<template>
    <div class="tianjianxuanran">
        <h3>条件渲染</h3>
        <div v-if="flag">看见我吧</div>
        <div v-else>没有看见我</div>
        <div v-if="type === 'A'">A</div>
        <div v-else-if="type === 'B'">B</div>
        <div v-else-if="type === 'C'">C</div>
        <div v-else>NOT ABC</div>
        <div v-show="flag1">看见看见</div>
        <hr>
    </div>
</template>

<script>
export default {
    name: "tianjianxuanran",
    data() {
        return {
            flag: true,
            type: "D",
            flag1: false
        }
    },
}
</script>

<style scoped>
.tianjianxuanran {
    color: red;
}
</style>