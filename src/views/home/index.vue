<template>
    <div class="wrap">
        <header class="header">
            <h2>多加网</h2>
        </header>
        <main class="main">
            <div class="top-box">
                <div class="image">

                </div>
                <div class="content">
                    <dl v-for="lists in listdata" :key="lists.id" class="coned">
                        <dt>
                            {{lists.img}}
                        </dt>
                        <dd>
                            {{lists.des}}
                        </dd>
                    </dl>
                </div>
            </div>
         <swiper :options="swiperOption" class="bannner">
            <swiper-slide v-for="slide in swiperSlides" :key="slide.id">
                <div class="con">{{slide}}</div>
            </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
        </main>
        <vfoot></vfoot>
       
    </div>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import 'swiper/dist/css/swiper.css'
import vfoot from '../../components/foot/inedx'
export default {
     data() {
      return {
        swiperOption: {
          pagination: {
            el: '.swiper-pagination'
          }
        },
        swiperSlides: [1, 2, 3, 4, 5],
           listdata:[
               {
                   img:'1',
                   des:'成绩奖励',
                   id:0
               },
                {
                   img:'2',
                   des:'成绩奖励',
                   id:1
               },
                {
                   img:'3',
                   des:'成绩奖励',
                   id:2
               },
                {
                   img:'4',
                   des:'成绩奖励',
                   id:3
               },
                {
                   img:'5',
                   des:'成绩奖励',
                   id:4
               },
                {
                   img:'6',
                   des:'成绩奖励',
                   id:5
               }, {
                   img:'7',
                   des:'成绩奖励',
                   id:6
               },
                {
                   img:'8',
                   des:'成绩奖励',
                   id:8
               }
           ]
      }
   
    },
    components:{
        vfoot,
         swiper, 
         swiperSlide
    }
}
</script>

<style>

</style>
