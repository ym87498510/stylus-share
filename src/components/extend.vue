<template>
    <div>
        <p class="message">我是一般的消息</p>
        <p class="warning">我是警告信息</p>
        <p class="error">我是错误信息</p>
        <p class="fatal">我是致命错误</p>
    </div>
</template>

<script type="text/ecmascript-6">
    export default {
        name: 'extend',
        data() {
            return {}
        }
    }
</script>

<style lang="stylus" rel="stylesheet/stylus" scoped>
    /*div
        width 7.5rem
        height 2rem
        .message
            padding 10px
            border 1px solid #ddd
        .warning
            // 可以这样写,stylus的继承支持标签嵌套，sass中会报错
            @extend div .message
            color #e25730*/


    /*这是一个更复杂的例子*/

    red = #E33E1E
    yellow = #E2E21E

    .message
        padding: 10px
        font: .5rem Helvetica
        border: 1px solid #eee

    .warning
        @extends .message
        border-color: yellow
        background: yellow + 70%

    .error
        @extends .message
        border-color: red
        background: red + 70%

    .fatal
        @extends .error
        font-weight: bold
        color: red
</style>
