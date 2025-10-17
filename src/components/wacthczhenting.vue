<template>
    <div class="watchczhenting">
        <h3>watch侦听</h3>
        <!-- 只能侦听data中的数据变化 -->
        <p>{{ message }}</p>
        <button @click="update">修改数据</button>
        <hr>
    </div>
</template>

<script>
export default {
    name: "14watchczhenting",
    data() {
        return {
            message: 'hello world'
        }
    },
    components: {},
    methods: {
        update() {
            this.message = 'hello vue'
        }
    },
    watch: {
        // 函数名称与data中的属性名称相同，newValue, oldValue为参数,newValue为新值，oldValue为旧值
         message(newValue, oldValue) {
            // 数据发生变化，自动执行的函数
            console.log(newValue, oldValue)
        }
    }
}
</script>

<style scoped>
.watchczhenting {
    color: thistle;
}
</style>
