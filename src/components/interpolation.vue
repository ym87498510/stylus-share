<template>
    <div>
        <table>
            <tbody>
            <tr>
                <td>12345</td>
                <td>67890</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>67890</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>67890</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>67890</td>
            </tr>
            <tr>
                <td>12345</td>
                <td>67890</td>
            </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    export default {
        name: 'Interpolation'
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='stylus' rel="stylesheet/stylus" scoped>
    /*插值的一个作用是写浏览器前缀，但目前使用较少*/
    vendor(prop, args)
        -webkit-{prop} args
        -moz-{prop} args
        {prop} args

    box-shadow()
        vendor('box-shadow', arguments)

    div
        border 1px solid #ddd
        box-shadow 2px 2px 2px 2px red
        padding 10px
    /*选择器也可以使用插值,for in 是一个迭代器*/
    table
        for row in 1 2 3 4 5
            tr:nth-child({row})
                height: 10px * row
                font-size 10px * row

</style>
