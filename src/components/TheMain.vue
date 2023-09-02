<script>
    import GenericSection from './GenericSection.vue';
    import InvertedDoubleElements from './InvertedDoubleElements.vue';
    import CarouselSection from './CarouselSection.vue';
    import PriceSection from './PriceSection.vue';
    import ReviewSection from './ReviewSection.vue';
    import TestimonialCard from './TestimonialCard.vue';
    import Clients from './Clients.vue';
    

    export default{
        components:{
            GenericSection,
            InvertedDoubleElements,
            CarouselSection,
            PriceSection,
            ReviewSection,
            TestimonialCard,
            Clients,
        }
    }
</script>

<template>
    <main>
        <GenericSection></GenericSection>
        <InvertedDoubleElements></InvertedDoubleElements>
        <CarouselSection></CarouselSection>
        <PriceSection></PriceSection>
        <ReviewSection></ReviewSection>
        <TestimonialCard></TestimonialCard>
        <Clients></Clients>
    </main>
    


</template>

<style lang="scss" scoped>
    section{
        padding-left: 130px;
        padding-right: 130px;
    }
</style>