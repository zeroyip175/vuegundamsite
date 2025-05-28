<template>
    <div class="profile-page">
        <section class="section-profile-cover section-shaped my-0">
            <div class="shape shape-style-1 shape-primary shape-skew alpha-4">
            </div>
        </section>
        <div class="container ct-example-row">
        <div class="row">
            <div class="col">
        <h1>GundamDetails</h1>
        <p>The Gundam id is {{ $route.params.id}}</p>
        <img :src="$route.params.img" alt="Gumdan Img">
        <h2>Data</h2>
        <p>{{ $route.params.descption }}</p>
        <h2>Department</h2>
        <img src="/img/brand/blue.png" alt="Depart img">
        </div>
        </div>
        </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            id: this.$route.params.id,
            img: this.$route.params.img,
            descption: this.$route.params.descption,
            department: this.$route.params.department
        }
    }
};
</script>
<style>
</style>
