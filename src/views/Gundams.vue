<template>
    <div class="profile-page">
        <section class="section-profile-cover section-shaped my-0">
            <div class="shape shape-style-1 shape-primary shape-skew alpha-4">
            
            </div>
        </section>
                <h1>Gundams</h1>
                <div v-for="gundam in gundams" :key="gundam.id">
                    <router-link :to="{name: 'gundamsdetails', params: {id: gundam.id, img: gundam.img, descption:gundam.descption}}">
                        <h2>Name: {{ gundam.title }}</h2>
                        <img :src="gundam.img" alt="gundam img"/>
                        <p v-show="false">{{ gundam.descption }}</p>
                        
                    </router-link>
                </div>
                

    </div>
</template>
<script>
export default {
    data(){
        return{
            gundams: [
                {title: 'Destiny Gundam Spec II', id: 1, details: 'ZGMF/A-42S2',img: '/img/gundams/gundam_1.jpg', descption: 'A new aircraft given to Shin Asuka in "Mobile Suit Gundam SEED Destiny". The large beam sword on the back that can be deployed as set, the long-range beam cannon, the beam boomerangs on both shoulders, and the armaments that exist in the deployment setting of the wings are reproduced as much as possible.'},
                {title: 'Strike Freedon Gundam', id: 2, details: 'ZGMF-X20A', img: '/img/gundams/gundam_3.jpg', descption: 'Strike Freedom Gundam is the last trump card developed in order to breakthrough the conflicted situation of ZAFT and Earth Alliance Forces. Due to the installation of a new engine, its combat capability is several times higher than the Freedom Gundam. Its joints are gold colored. It is piloted by Kira Yamato.'},
                {title: '∞ Justice Gundam Type II', id: 3, details: 'ZGMF-X191M2', img:'/img/gundams/gundam_2.jpg', descption: 'The ∞ Justice Type II s back-mounted lifter unit, it is armed with two MA-M50E3F High-Energy Long-Range Beam Cannons, two AGMRAAM Scorpio missile launchers, and Beam Riser wings that are capable of both ranged and melee combat.'},
            ],
        }
    }
};
</script>
<style>
</style>
