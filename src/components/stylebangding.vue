<template>
    <div class="stylebangding">
        <h3>style样式绑定</h3>
        <p :style="{color: activeColor, fontSize: fontSizeNum + 'px'}">style绑定样式1</p>
        <p :style="styleObject">style绑定样式2</p>
        <hr>
    </div>
</template>

<script >
export default {
    name: "13stylebangding",
    data() {
        return {
            activeColor: 'blue',
            fontSizeNum: 30,
            styleObject: {
                color: 'white',
                fontSize: '35px'
            }
        }
    },
    components: {},
    methods: {}
}
</script>

<style scoped>
.stylebangding {
    color: chartreuse;
}

</style>
