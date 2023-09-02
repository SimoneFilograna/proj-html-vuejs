<script>
    export default{

    }
</script>

<template>
    <div class="footer-container">
        <div class="row row-cols-4 g-5">

            <!-- img col -->

            <div class="col">
                <div class="card">
                    <img src="../assets/white-logo-2.png" alt="" class="img-logo-foot pb-5">                       
                    <div class="card-body">
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                </div>
            </div>

            <!-- first col -->

            <div class="col">
                <div class="card">
                    <h4 class="pb-4 text-white">Quick Links</h4>
                    <ul>
                        <li>
                            <a href="#">Services</a>
                        </li>
                        <li>
                            <a href="#">Contact</a>
                        </li>
                        <li>
                            <a href="#">Blog</a>
                        </li>
                        
                    </ul>
                </div>
            </div>

            <!-- second col -->

            <div class="col">
                <div class="card">
                    <h4 class="pb-4 text-white">Resources</h4>
                    <ul>
                        <li>
                            <a href="#">Art Design</a>
                        </li>
                        <li>
                            <a href="#">Computer</a>
                        </li>
                        <li>
                            <a href="#">IT News</a>
                        </li>
                        <li>
                            <a href="#">Networking</a>
                        </li>
                        <li>
                            <a href="#">Web Security</a>
                        </li>
                        
                    </ul>
                </div>
            </div>

            <!-- third col  -->

            <div class="col">
                <div class="card">
                    <h4 class="pb-4 text-white">Contac Us</h4>
                    <p><strong> Address:</strong> Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051</p>
                    <p><strong> Phone:</strong> +99 (0) 101 0000 888</p>
                    <p><strong> Email:</strong> Info@yourdomaimcom</p>
                    
                    
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";

    .footer-container{
        padding-bottom: 3rem;
        padding-top: 10rem;
        padding-left: 120px;
        padding-right: 120px;
        @include mixins.blue-background;

        .card{
            padding: 1rem;
            border: 0;
            background-color: transparent;
            color: #617a9a;

            strong{
                color: white;
            }

            .img-logo-foot{
                width: 150px;
            }

            ul{
                list-style: none;
                padding: 0;
                line-height: 40px;

                a{
                    text-decoration: none;
                    color: #617a9a;

                &:hover{
                    color: variables.$over-color-text;
                }
                }
            }
        }
    }

</style>