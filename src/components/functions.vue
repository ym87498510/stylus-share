<template>
    <div>
        <p class="first"></p>
        <p class="second"></p>
    </div>
</template>

<script type="text/ecmascript-6">
    export default {
        name: 'function',
        data() {
            return {}
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
    // 计算从设计稿到rem的尺寸
    ctr(n)
        (n/100)rem

    add(a,b=a)
        a = unit(a, '') //去除单位，也可以换成px
        b = unit(b, '')
        ctr(a + b)


    sizes() //可以返回多个值
        .1rem .2rem .3rem .4rem

    $commBorder()
        border-left ctr(10) solid #ddd
        border-top ctr(20) solid #ddd
        border-right ctr(30) solid #ddd
        border-bottom ctr(40) solid #ddd
        box-shadow 5px 5px 5px 5px #28b238

    div
        .first
            width ctr(100)
            height ctr(50)
            background blue
            margin add(20)
            $commBorder()
        .second
            width ctr(50)
            height ctr(100)
            background yellow
            margin sizes()[1]
            $commBorder()
</style>
