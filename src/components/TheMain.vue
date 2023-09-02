<script>
    import GenericSection from './GenericSection.vue';
    import InvertedDoubleElements from './InvertedDoubleElements.vue';
    import CarouselSection from './CarouselSection.vue';
    import PriceSection from './PriceSection.vue';
    import ReviewSection from './ReviewSection.vue';
    import TestimonialCard from './TestimonialCard.vue';

    export default{
        components:{
            GenericSection,
            InvertedDoubleElements,
            CarouselSection,
            PriceSection,
            ReviewSection,
            TestimonialCard,
        }
    }
</script>

<template>
    <GenericSection></GenericSection>
    <InvertedDoubleElements></InvertedDoubleElements>
    <CarouselSection></CarouselSection>
    <PriceSection></PriceSection>
    <ReviewSection></ReviewSection>
    <TestimonialCard></TestimonialCard>


</template>

<style lang="scss" scoped>
    section{
        padding-left: 130px;
        padding-right: 130px;
    }
</style>