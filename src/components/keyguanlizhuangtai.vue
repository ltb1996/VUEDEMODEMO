<template>
    <div class="keyguanlizhuangtai">
        <h3>key属性添加到v-for中</h3>
        <div v-for="(value, index) in names" :key="index">{{ value }}</div>
        <!-- 推荐在任何可行的时候为 v-for 提供一个 key attribute，key 绑定的值期望是一个基础类型的值，例如字符串或 number 类型。 -->
         <!-- 最好不要使用index作为 key 值，我们要确保每一条数据的唯一索引不会发生变化，
          因为这会基于数组的顺序来决定元素。如果数组的顺序发生变化，这些 key 值就变成了无效的，这可能会导致渲染结果出错。 -->
        <div v-for="value in results" :key="value.gkey">
            <p>{{ value.name }}</p>
            <img :src="value.img" :alt="value.name"></img>
        </div>
        <hr>

    </div>
</template>

<script>
export default {
    name: "5keyguanlizhuangtai",
    data() {
        return {
            names: ["zhangsan1111", "lisi1111", "wangwu1111"],
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
        }
    },
    components: {},
    methods: {}
}
</script>

<style scoped>
.keyguanlizhuangtai {
    color: yellow;
}
</style>
