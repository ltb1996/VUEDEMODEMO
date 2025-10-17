<template>
    <div class="biaodanshujubangding">
        <h3>表单数据绑定</h3>
        <form>
            <input type="text" v-model.lazy="lazya"></input>
            <p>{{ lazya }}</p>
            <input type="text" v-model="message"></input>
            <p>{{ message }}</p>
            <!-- 注意label的for属性与input的id属性要一致 -->
            <input type="checkbox" id="checkbox" v-model="checked"></input>
            <label for="checkbox">{{ checked }}</label>
            
        </form>

    </div>
</template>

<script >

export default {
    name: "15biaodanshujubangding",
    data() {
        return {
            message: "hellosss",
            checked: false,
            lazya: "lazyaaaaaaa"
        }
    },
    components: {},
    methods: {}
}
</script>

<style scoped>
.biaodanshujubangding {
    color: red;
}

</style>
