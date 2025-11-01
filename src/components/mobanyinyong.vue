<template>
    <div class="mobanyinyong">
        <h3>模板引用</h3>
        <div class="container" ref="container">{{ content }}</div>
        <button @click="getContainer">获取元素</button><br>
        <input type="text" ref="username">

        <hr>
    </div>
</template>

<!-- 内容改变： {{}} 
     属性改变：v-bind
    事件： v-on:click
    如果没有特别的需求，不要操作dom
-->

<script>
export default {
    name: "16mobanyinyong",
    data() {
        return {
            content: "hello world"
        }
    },
    methods: {
        getContainer() {
            console.log(this.$refs.container);
            // innerHTML属性是原生js的属性
            console.log(this.$refs.container.innerHTML = "hahahahhaha");
            console.log(this.$refs.username.value);
        }
    }
}
</script>

<style scoped>
.mobanyinyong {
    color: green;
}
</style>