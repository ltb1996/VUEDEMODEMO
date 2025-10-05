<template>
    <div class="shuxingbangding">
        <H3>属性绑定</H3>
        <p :id="dynamicId" :class="dynamicClass" :title="titleaaa" :aaa="aaa">测试测试</p>
        <button :disabled="isButtonDisabled">button</button>
        <div v-bind="objectOfAttrs">啊是大多数</div>
    </div>
</template>

<script >

export default {
    name: "shuxingbangding",
    data() {
        return {
            dynamicId: "id1",
            dynamicClass: "class1",
            titleaaa: "标题",
            aaa: null,
            isButtonDisabled: false,
            objectOfAttrs: {
                class: "id1",
                id: "class1"
            }
        }
    },
}
</script>

<style scoped>
.shuxingbangding{
    color: white;
}
.class1 {
    color: aqua;
}

</style>
