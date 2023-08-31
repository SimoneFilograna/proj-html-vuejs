<script>
    import Navbar from "./Navbar.vue";

    export default{
        components: {
            Navbar,
        }
    }
</script>

<template>
    <header>
        <div class="jumbotron">

            <div class="container-fluid">

                <Navbar></Navbar>

                <div class="introduce-container">

                </div>

            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";

    .jumbotron{
        @include mixins.blue-background;
        height: 200px;
        padding-left: 130px;
        padding-right: 130px;
    }
</style>