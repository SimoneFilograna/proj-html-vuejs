<script>
    import GenericSection from './GenericSection.vue';
    import InvertedDoubleElements from './InvertedDoubleElements.vue';
    import CarouselSection from './CarouselSection.vue';

    export default{
        components:{
            GenericSection,
            InvertedDoubleElements,
            CarouselSection,
        }
    }
</script>

<template>
    <GenericSection></GenericSection>
    <InvertedDoubleElements></InvertedDoubleElements>
    <CarouselSection></CarouselSection>

</template>

<style lang="scss" scoped>
    section{
        padding-left: 130px;
        padding-right: 130px;
    }
</style>