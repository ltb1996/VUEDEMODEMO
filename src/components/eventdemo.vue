<template>
    <div class="eventDemo">
        <h3>事件传参例子</h3>
        <!-- 想要点击哪个名字控制台就显示出哪个名字，不是点击一次全部显示 -->
        <p v-for="(value, index) in names" :key="index" @click="getName(value, $event)">{{ value }}</p>
        <hr>
    </div>
</template>

<script>
export default {
    name: "8eventDemo",
    data() {
        return {
            names: ['张三', '李四', '王五']
        }
    },
    components: {},
    methods: {
        getName(name, e) {
            console.log(name, "45454545name")
            console.log(e)
        }
    }
}
</script>

<style scoped>
.eventDemo {
    color: aquamarine;
}
</style>
