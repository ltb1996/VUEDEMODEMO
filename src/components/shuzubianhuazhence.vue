<template>
    <div class="shuzubianhuazhence">
        <h3>数组变化侦测</h3>
        <!-- 变更方法：push, unshift, pop, shift, splice, sort, reverse  (改变原数组，数组变化，页面UI发生变化) -->
        <!-- 替换一个数组： filter, map, slice, concat （不改变原数组，数组变化，页面UI不变化）-->
        <button @click="addData">添加数据</button>
        <ul>
            <li v-for="(value, index) in names" :key="index">{{ value }}</li>
        </ul>
        <button @click="hebingshuzu">合并数组</button>
        <h1>数组1</h1>
        <p v-for="(value, index) in arr1" :key="index">{{ value }}</p>
        <h1>数组2</h1>
        <p v-for="(value, index) in arr2" :key="index">{{ value }}</p>
        <hr>
    </div>
</template>

<script>
export default {
    name: "10shuzubianhuazhence",
    data() {
        return {
            names: ['张三', '李四', '王五'],
            arr1: [1, 2, 3],
            arr2: [4, 5, 6]
        }
    },
    components: {},
    methods: {
        addData() {
            // 引起ui自动更新
            // this.names.push('赵六')
            // 不会引起ui自动更新
            this.names.concat(['赵六']);
            this.names = this.names.concat(['赵六']);
            console.log(this.names.concat(['赵六']));
        },
        hebingshuzu() {
            // this.arr1 = [...this.arr1, ...this.arr2];
            this.arr1 = this.arr1.concat(this.arr2);
        }
    }
}
</script>

<style scoped>
.shuzubianhuazhence {
    color: rosybrown
}
</style>
