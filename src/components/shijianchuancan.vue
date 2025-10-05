<template>
    <div class="shijianchuancan">
        <h3>事件传参</h3>
        <button @click="count">Add 12222</button>
        <p>Count is: {{ countNum }}</p>

        <button @click="newCount('hello')">newCount 222</button>
        <p>newCount is: {{ newCountNum }}</p>

        <hr>
    </div>
</template>

<script>
export default {
    name: "shijianchuancan",
    data() {
        return {
            countNum: 0,
            newCountNum: 2
        }
    },
    components: {},
    methods: {
        // event对象
        count(e) {
            // vue中的event对象就是原生jsz中的event对象
            console.log(e, 'eeeeeeeeeeeeeeee');
            console.log(e.target, 'targettttt');
            console.log(e.currentTarget, 'currentTargettttt');
            console.log(e.target.innerHTML = "ADD" + this.countNum);
            e.target.innerHTML = "ADD" + this.countNum;
            this.countNum++;
        },
        newCount(msg) {
            console.log(msg, '+++++++++msg');
        }
    }
}
</script>

<style scoped>
.shijianchuancan {
    color: darkcyan;
}
</style>
