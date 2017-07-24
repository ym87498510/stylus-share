<template>
    <div>
        <p>我有背景</p>
    </div>
</template>

<script type="text/ecmascript-6">
    export default {
        name: 'mixins',
        data() {
            return {}
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
    // mixin和function 本质是一致的

    // 适用于加浏览器前缀,建议不要破坏原来的值类型
    background()
        background-color arguments[0]
        background-position arguments[3] arguments[4]
        background-size arguments[1] arguments[2]
        // 这只是举个例子
        -webkit-background-color arguments[0]

    div
        p
            background #999 100% 100% left center

    // 混合书写的形式可以嵌套，这是一个官方例子：创建内联comma-list()（通过inline-list()）以及逗号分隔的无序列表。
    inline-list()
        li
            display inline

    comma-list()
        inline-list()
        li
            &:after
                content ', '
            &:last-child:after
                content ''

    ul
        comma-list()
</style>
