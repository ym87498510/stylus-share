<template>
    <div class="wrapper">
        <p class="text">stylus可以使用变量</p>
    </div>
</template>

<script>
    export default {
        name: 'variables'
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' rel="stylesheet/stylus" scoped>
    /*可以指定变量，调用*/
    font-size = 20px

    .wrapper
        font font-size Arial, 'Microsoft Sans Serif'

    /*变量可以组合表达式列表*/
    font = font-size Arial, 'Microsoft Sans Serif'

    .wrapper
        p
            font font "Mishafi Gold"

    /*stylus原本没有限制变量的声明形式，但最好加上$,以做区分*/
    $font-size = 20px



    /*属性查找,举个元素上下左右居中的例子*/
    .wrapper
        position relative
        width w = 7.5rem  /*在写属性值是声明变量（局部变量），变量有作用域，逐级向上查找*/
        height (w / 3 * 2)
        background #0fdb49
        p
            position absolute
            background #F2F6FA
            top 50%
            left 50%
            width 3rem
            height (@width / 3) /*注意运算符和参数间的空格*/
            margin-left -(@width / 2)
            margin-top -(@height / 2)
    /*根据其他属性的值设置属性*/

    position()
        position arguments
        z-index 1 unless @z-index

    .wrapper
        p
            /*注释我试试*/
            /*z-index 20*/
            position absolute

</style>
