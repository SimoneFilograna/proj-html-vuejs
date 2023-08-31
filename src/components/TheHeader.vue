<script>
    export default{

    }
</script>

<template>
    <header>
        <div class="jumbotron">

            <div class="container">
                <div class="navbar">

                </div>

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
    }
</style>