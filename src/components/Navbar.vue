<script>    
    export default {
        data(){
            return{
                linkList: [ 'Home','About', 'Service', 'Blog', 'Contact', 'Portfolio' ]
            }
        }
    }
</script>

<template>
    <div class="navbar-container">

        <div class="logo-container flex-grow-1">
            <img src="../assets/white-logo-2.png" class="logo-top" alt="">
        </div>

        <div class="menu-container">
            <ul class="d-flex gap-4 align-items-center">
                <li v-for="singlelink in linkList">
                    <a href="#"> {{ singlelink }}</a>
                </li>
            </ul>
        </div>

        <div class="button-container ps-5">
            <button type="button" class="btn btn-primary my-button">Sign In</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    .navbar-container{
        color: white;
        display: flex;
        align-items: center;
        padding-top: 1.5rem;
        .logo-top{
            width: 130px;
        }

        .menu-container{
            ul{
                list-style: none;
                padding-top: 1rem;
                a{
                    text-decoration: none;
                    color: white;
                }
            }
        }

        
        .my-button{
            @include mixins.blue-button;

        &:hover{
            @include mixins.red-hover;
        }
        }

    }
</style>