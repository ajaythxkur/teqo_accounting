<template>
    
        <div class="col-12 col-md-12 col-lg-12">
            <div class="services-description text-center mb-lg-5">
                <h4 class="text-capitalize">{{heading}}</h4>
                <h3>{{description}}</h3>
            </div>
            <!-- services-description -->
        </div>
</template>
<script>
    export default {
        name: 'MainHeading',
        props: {
            heading: String,
            description: String
        }
    }
</script>
<style>
.services-description h4{
    font-weight: 500;
    font-size: 19px;
    color: var(--tq-orange);
}
.services-description h3{
    font-weight: 600;
    font-size: 30px;
    color: var(--tq-blue);
    font-weight: 600;
    margin-bottom: 20px;
}
</style>