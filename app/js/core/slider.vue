<!-- 组件说明 -->
<template>
    <section :class='cname' id="cSlider">
        <swiper :options = "options" :not-next-tick = "options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination" v-if="options.pagination"></div>
        </swiper>
    </section>
</template>

<script>
    import {swiper,swiperSlide} from 'vue-awesome-swiper'
    export default {
        props:{
            cname:{
                type: String,
                default: ''
            },
            options:{
                type: Object,
                default(){
                    return {
                        autoplay: true,
                        loop: true,
                        pagination: {
                            el: ".swiper-pagination"
                        },
                        notNextTick: false,
                    }
                }
            },
            items:{
                type: Array,
                default(){
                    return []// {href:'',src:''}
                }
            }
        },
        components: {
            swiper,
            swiperSlide
        },
        data () {
            return {

            };
        },
        computed: {

        },
        methods: {

        },
    }
</script>
<style lang='scss'>
@import '~swiper/dist/css/swiper.css';
 .swiper-pagination-bullet{
    width: 12px;
    height: 12px;
  }
  #cSlider{
      margin-top: 100px;
  }
</style>