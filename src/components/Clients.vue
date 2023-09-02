<script>
    export default{
        data(){
            return{
                logoImgs: [
                    "../assets/client-1-1.png",
                    "../assets/clienty-2.png",
                    "../assets/clienty-3.png",
                    "../assets/clienty-4.png",
                    "../assets/client-5.png"
                ]
            }
        },
        methods:{
            getImg(img){
                return new URL(img, import.meta.url).href
            }
        }
    }
</script>

<template>
    <section>
        <div class="logo-container d-flex justify-content-around" >
            <img :src="getImg(singleLogo)" alt="" v-for="singleLogo in logoImgs" class="logo">
        </div>
    </section>
</template>

<style lang="scss">
    .logo-container{
        margin-top: 14rem;
        margin-bottom: 14rem;

        .logo{
            object-fit: contain;
        }
    }
</style>