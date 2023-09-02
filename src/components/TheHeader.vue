<script>
    import Navbar from "./Navbar.vue";
    import DoubleElements from "./DoubleElements.vue";

    export default{
        components: {
            Navbar,
            DoubleElements
        }
    }
</script>

<template>
    <header>
        <div class="jumbotron">

            <div>

                <Navbar></Navbar>

                <DoubleElements></DoubleElements>

            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";

    .jumbotron{
        @include mixins.blue-background;
        padding-left: 130px;
        padding-right: 130px;
    }
</style>