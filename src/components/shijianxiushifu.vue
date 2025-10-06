<template>
    <div class="shijianxiushifu">
        <h3>事件修饰符</h3>
        <!-- <a @click="click11" href="https://www.baidu.com" >百度百度</a> -->
         <!-- 阻止事件默认行为 -->
        <a @click.prevent="click11" href="https://www.baidu.com" >百度百度</a>
        <!-- 阻止事件冒泡 -->
        <div @click="clickDiv">
            <!-- <p @click="clickP">测试冒泡</p> -->
            <p @click.stop="clickP">测试冒泡</p>
        </div>

        <hr>
    </div>
</template>

<script >
export default {
    name: "shijianxiushifu",
    data() {
        return {}
    },
    components: {},
    methods: {
        click11(e) {
            // 阻止默认行为
            // e.preventDefault();
            console.log("点击了")
        },
        clickDiv() {
            console.log("DIV");
        },
        clickP(e) {
            // e.stopPropagation();
            console.log("P");
        }
    }
}
</script>

<style scoped>
.shijianxiushifu {
    color: chartreuse;
}

</style>
