<template>
    <div class="jisuanshuxing">
        <h3>计算属性</h3>
        <p>{{ content.name }}</p>
        <div>{{ content.text.length > 0 ? 'yes' : '无数据' }}</div>
        <!-- 计算属性不需要加括号，直接写名字即可 -->
        <div>{{ isContentTextEmpty }}</div>
        <!-- 函数或方法需要加括号，直接写名字即可 -->
        <div>{{ isContentTextEmptys() }}</div>
    </div>
</template>

<script>
export default {
    name: "jisuanshuxing",
    data() {
        return {
            content: {
                name: "abc",
                text: ["1", "2", "3"]
            }
        }
    },
    // 计算属性
    computed: {
        isContentTextEmpty() {
            return this.content.text.length > 0 ? 'yes' : '无数据';
        }
    },
    // 放函数或方法
    methods: {
        isContentTextEmptys() {
            return this.content.text.length > 0 ? 'yes' : '无数据';
        }
    }
}
</script>

<style scoped>
.jisuanshuxing {
    color: turquoise;
}
</style>
