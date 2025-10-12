<template>
    <div class="classbangding">
        <H3>CLASS动态绑定</H3>
        <p :class="myClass"></p>
        <h5>绑定对象示例</h5>
        <p :class="{'active':isActive, 'text-danger':hasError}">class样式绑定1</p>
        <div :class="classObject">
            class样式绑定2
        </div>
        <h5>绑定数组示例</h5>
        <p :class="[arrActive, arrHasError]">class样式绑定3</p>

        <p :class="[isActive ? 'active' : '']">class样式绑定4</p>

        <!-- 数组和对象一起使用嵌套过程中，只能是数组嵌套对象，对象嵌套数组无效 -->

        <p :class="[isActive ? 'active' : '', { 'text-danger': hasError }]">class样式绑定5</p>
        <hr>
    </div>
</template>

<script >
export default {
    name: "12classbangding",
    data() {
        return {
            myClass: "demo",
            isActive: true,
            hasError: true,
            classObject: {
                'active': true,
                'text-danger': true
            },
            arrActive: 'active', //数组绑定
            arrHasError: 'text-danger'
        }
    },
    components: {},
    methods: {}
}
</script>
<style scoped>
.classbangding {
    color: teal;
}

.active {
    
    font-size: 35px;
}

.text-danger{
    color: red;
}

</style>