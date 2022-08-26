<template>
    <div class="carousel-content">

        <carousel
        class="carousel-slider owl-theme" 
     :autoplayTimeout="5000" :loop="true"
    :autoplay="true" :fluid-speed="true" :center="true" :margin="15" 
    :responsive="{0:{items: 1, nav:false}, 601:{items:5, nav: true}, 1240:{items: 5, nav:true}}"
        >
        
       <div v-for="(slide, idx) in carouselItems" :key="idx" class="carousel-wrapper" :class="idx == 2 ? 'second-item' : ''"
        :style="{'background-image' : 'url(' + require('@/assets/Content/' + slide.background_img  ) + ')',
                'background-repeat' : 'no-repeat',
                'background-size' : 160 + 'px',
                'background-position' : 'center'
        }" 
        :ref="`item-${slide.id}`" 
        >
            <img :src="require('@/assets/Content/' + slide.img)" alt="">
            <div class="carousel-title">
                <h3>{{slide.name}}</h3>
            <p>{{slide.title}}</p>
            <button>{{slide.button  }}</button>
            </div>
            
        </div>  
        
        </carousel>

    </div>
</template>
<script>
import carousel from 'vue-owl-carousel'
export default {
    name: 'carousel-container',
    components: {carousel},
    data(){
        return{
            carouselItems: [
        {
          id: 1,
          name: "Футбол",
          img: "img1.png",
          background_img: "Vector1.png",
          title:
            "Футбо́л (англ. football от foot «ступня» + ball «мяч») — командный вид спорта, в котором целью является забить ...",
          button: "Подробнее",
        },
        {
          id: 3,
          name: "Теннис",
          img: "img2.png",
          background_img: "Vector2.png",
          title:
            "Те́ннис (англ. tennis) или большо́й теннис — вид спорта, в котором соперничают либо два игрока ...",
          button: "Подробнее",
        },
        {
          id: 4,
          name: "Баскетбол",
          img: "img3.png",
          background_img: "Vector3.png",
          title:
            "Баскетбо́л — спортивная командная игра с мячом, в которой мяч забрасывают руками в кольцо соперника.",
          button: "Подробнее",
        },
        {
          id: 5,
          name: "Хоккей",
          img: "img4.png",
          background_img: "Vector4.png",
          title:
            "Хокке́й (англ. hockey) — семейство игр на ледовой, тартановой, пластиковой, деревянной или травяной площадке, в котором две команды ...",
          button: "Подробнее",
        },
        {
          id: 6,
          name: "Бокс",
          img: "img5.png",
          background_img: "Vector5.png",
          title:
            "Бокс (от фр. boxe — «бокс» и boxeur — «боксёр», которые происходят от англ. to box — «драться на ринге», «боксировать»...",
          button: "Подробнее",
        },
      ],
        }
    },
    mounted(){
      this.catchItem()
    },
    methods:{
      catchItem(){
        // const not = document.getElementsByClassName('second-item')
        // console.log(not)
        this.carouselItems.forEach(elem => {
          let item = this.$refs[`item-${elem.id}`]
          console.log(item)

        })
      }
    }
}
</script>