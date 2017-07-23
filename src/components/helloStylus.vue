<template>
    <div class="hello">
        <h1>{{ msg }}</h1>
        <p>富有表现力</p>
    </div>
</template>

<script>
    export default {
        name: 'hello',
        data() {
            return {
                msg: 'Hello Stylus'
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' rel="stylesheet/stylus" scoped>
/*
* 书写风格
* 推荐缩进的风格
* 兼容原声CSS写法
* 可省略大括号后、冒号、分号，注：省略选择器之间的逗号需要换行
* 支持类似sass的嵌套
*/
.hello {
    margin 0 auto
    font-size .4rem
    display flex
    flex-direction column
    align-items center
    h1 {
        font-size: .9rem;
    }
    p {
        margin-top .2rem
        color red
    }
}
</style>
