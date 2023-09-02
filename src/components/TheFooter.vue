<script>
    import TopFooter from './TopFooter.vue';

    export default{
        components:{
            TopFooter,
        }
    }
</script>

<template>
    <footer>
        <TopFooter></TopFooter>
    
        <div class="credits">
    
        </div>
    </footer>


</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";

    footer{
        padding-left: 120px;
        padding-right: 120px;
        @include mixins.blue-background;
    }
</style>