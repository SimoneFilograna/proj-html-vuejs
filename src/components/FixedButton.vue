<script>
    export default{

    }
</script>

<template>

                        <!-- MID BUTTON -->

    <div class="fixed-container-mid text-white">

        <!-- first-link -->

        <div class="link-containers d-flex align-items-center gap-2">
            <i class="fa-solid fa-table-cells-large"></i>
            <span>Browse Demos</span>
        </div>

        <!-- second link -->

        <div class="link-containers d-flex align-items-center gap-2">
            <i class="fa-solid fa-bag-shopping"></i>
            <span>Buy Now!</span>
        </div>

        <!-- third link -->

        <div class="link-containers d-flex align-items-center gap-2">
            <i class="fa-solid fa-file-export"></i>
            <span>Export Section</span>
        </div>
    </div>



                <!-- BOTTOM BUTTON -->

    <div class="fixed-container-bottom d-flex align-items-center gap-4">

        <div class="arrow-container">
            <i class="fa-solid fa-arrow-up"></i>
        </div>

        <div class="chat-container text-white" >
            <i class="fa-regular fa-comment fa-flip-horizontal"></i>
        </div>
    </div>               
</template>

<style lang="scss" scoped>

    // container button mid
    .fixed-container-mid{
        z-index: 9999;
        position: fixed;
        right: 0;
        top: 50%;
        transform: translateY(-50%);

        .link-containers{
            cursor: pointer;
            margin-bottom: .3rem;
            width: 150px;
            background-color: #1b1b1b6c;
            border-top-left-radius: 15px;
            border-bottom-left-radius: 15px;
            padding: .8rem 0 .8rem 1rem;

        &:hover{
            background-color: #0d6efd;
        }

            i{
                font-size: 1.2rem;
            }

            span{
                font-size: .8rem;
            }

        }
    }

    // container button bottom

    .fixed-container-bottom{
        z-index: 9999;
        position: fixed;
        right: 3%;
        bottom: 5%;

        .arrow-container{
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: white;
            border: 1px solid black;
            border-radius: 50%;
            width: 50px;
            transition: background-color .5s cubic-bezier(0.47, 0, 0.745, 0.715);

        &:hover{
            background-color: #3d3d3d;
            color: rgb(255, 255, 255);
        }

            i{
                font-size: .9rem;
                padding: 1rem;
                
            }
        }

        .chat-container{
            cursor: pointer;
            background-color: #577eeb;
            border-radius: 50%;

        &:hover{
            background-color: #3e67d6;;
        }

            i{
                font-size: 1.8rem;               
                padding: 1.3rem;             
                aspect-ratio: 1/1;
            }
        }
    }


</style>