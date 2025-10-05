<template>
    <div class="liebiaoxuanran">
        <h3>列表渲染</h3>
        <div v-for="value in names">{{ value }}</div>
        <div v-for="(value, index) in names">{{ value }}--- {{ index }}</div>
        <div v-for="value in results">
            <p>{{ value.name }}</p>
            <img :src="value.img" :alt="value.name"></img>
        </div>
        <div v-for="(value, key, index) in myObject">{{ value }} --- {{ key }} --- {{ index }}</div>
        <hr>

    </div>
</template>

<script>
export default {
    name: "",
    data() {
        return {
            names: ["zhangsan", "lisi", "wangwu"],
            results: [
                {
                    "gkey": "102094960",
                    "qcmsint1": "0",
                    "w64": -1,
                    "gtype": "3",
                    "title": "双人游戏大全",
                    "url": "http://360game.360.cn/flash/102094960.html",
                    "gdata": "{\"type\":\"flashgame\",\"appid\":\"102094960\"}",
                    "name": "双人游戏大全",
                    "img": "//p0.qhimg.com/d/appstorage/74fcbb1da492f34b5ba49d99549afba0.png"
                },
                {
                    "gkey": "102144745",
                    "qcmsint1": "0",
                    "w64": -1,
                    "gtype": "3",
                    "title": "餐厅游戏大全",
                    "url": "http://360game.360.cn/flash/102144745.html",
                    "gdata": "{\"type\":\"flashgame\",\"appid\":\"102144745\"}",
                    "name": "餐厅游戏大全",
                    "img": "//p2.qhimg.com/t01c4a2f17a198def57.png"
                },
                {
                    "gkey": "102144642",
                    "qcmsint1": "0",
                    "w64": -1,
                    "gtype": "3",
                    "title": "火柴人游戏合集",
                    "url": "http://360game.360.cn/flash/102144642.html",
                    "gdata": "{\"type\":\"flashgame\",\"appid\":\"102144642\"}",
                    "name": "火柴人游戏合集",
                    "img": "//p1.qhimg.com/t0147f6ec029fefe8d7.png"
                }
            ],
            myObject: {
                title: 'How to do lists in Vue',
                author: 'Jane Doe',
                publishedAt: '2016-04-10'
            }
        }
    },
    components: {},
    methods: {}
}
</script>

<style scoped>
.liebiaoxuanran {
    color: slateblue;
}
</style>
