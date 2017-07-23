<template>
    <div class="selectors-wrapper">
        <div class="a"></div>
        <div class="b"></div>
        <p class="c"></p>
        <div class="d"></div>
    </div>
</template>

<script>
    export default {
        name: 'selectors'
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' rel="stylesheet/stylus" scoped>
    /* 函数中的写法，& 符号会指向其调用的父级 */
    box-shadow()
        -webkit-box-shadow arguments
        -moz-box-shadow arguments
        box-shadow arguments
        html.ie8 &,
        html.ie7 &,
        html.ie6 &
            border 3px solid arguments[length(arguments) - 1]

    .selectors-wrapper
        width w = 7.5rem
        background #d5d6c9
        box-sizing border-box
        padding .2rem
        display flex
        justify-content space-between
        div
            width 1rem
            height 1rem
            background #118d2b
            &.a
                border-bottom 5px solid red
                &:hover
                    width w = 1.5rem
                    height w
            &.b { /* 如果你喜欢，完全可以加上冒号、分号 */
                border-right: 5px solid blue
            }
            &:last-child
                border-bottom 5px solid pink
            &:hover
                width 1.2rem
                height @width

/* 有时候多行的选择器看起来像属性，可以用逗号分割开 */
    .selectors-wrapper p,
    form input
        width 1rem
        height 1rem
        background #6c2d8d

/* 调用函数方法 */
    .selectors-wrapper
        p
            box-shadow 2px 2px 5px #ee1c47


/* 函数中参数如果有表达式，需要用括号消除歧义,运算符和参数要有空格*/
    z-index(n)
        z-index (- n)

    .selectors-wrapper
        .box
            position absolute
            z-index(3)
</style>
