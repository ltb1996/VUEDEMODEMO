<template>
    <div class="shijianchuli">
        <h3>事件处理</h3>
        <h4>内联事件处理器</h4>
        <button @click="count++">Add 1</button>
        <p>Count is: {{ count }}</p>
        <h4>方法事件处理器</h4>
        <button @click="addCount()">Add 2</button>
        <p>Count is: {{ countNum }}</p>
        <hr>
    </div>
</template>

<script>
export default {
    name: "shijianchuli",
    data() {
        return {
            count: 0,
            countNum: 0
        }
    },
    components: {},
    // 所有的方法和函数都可以写在此处
    methods: {
        addCount() {
            // 读取到data中的数据的方案，this.countNum
            this.countNum += 2;
        }
    }
}
</script>

<style scoped>
.shijianchuli {
    color: brown;
}
</style>
