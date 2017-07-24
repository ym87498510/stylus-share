<template>
    <div id="app">
        <img src="./assets/stylus-logo.svg">
        <hello-stylus></hello-stylus>
        <!--选择器-->
        <!--<selectors></selectors>-->
        <!--变量-->
        <!--<variables></variables>-->
        <!--插值-->
        <!--<interpolation></interpolation>-->
        <!--混写-->
        <!--<mixins></mixins>-->
        <!--函数-->
        <!--<functions></functions>-->
        <!--继承-->
        <extend></extend>
    </div>
</template>

<script>
    import helloStylus from './components/helloStylus'
    import selectors from './components/selectors'
    import variables from './components/variables'
    import interpolation from './components/interpolation'
    import mixins from './components/mixins'
    import functions from './components/functions'
    import extend from './components/extend'
    export default {
        name: 'app',
        components: {
            helloStylus,
            selectors,
            variables,
            interpolation,
            mixins,
            functions,
            extend
        }
    }
</script>

<style lang='stylus' rel="stylesheet/stylus" scoped>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
    }

    img {
        display block
        width 5rem
        margin 1rem auto
    }
</style>
