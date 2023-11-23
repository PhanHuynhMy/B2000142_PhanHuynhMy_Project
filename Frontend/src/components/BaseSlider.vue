<template>
   <div class="slider-box">
      <div class="slider-content">
         <Splide :options="options" aria-label="My Favorite Images">
            <SplideSlide>
               <img src="https://file.hstatic.net/1000143422/file/ec-desktop_banner_1920x600px_31089e64f7aa41a59b90c472ff4ef0a0.png" alt="Sample 1" />
            </SplideSlide>
            <SplideSlide>
               <img src="https://file.hstatic.net/1000143422/collection/boots-nam_2cd4b87535c148b29ceac6f11e7e2c35_master.jpg" alt="Sample 1" />
            </SplideSlide>
            <SplideSlide>
               <img src="https://file.hstatic.net/1000143422/collection/new-nam_0a24aeec8e0243ed8bc26c7387636ed6_master.jpg" alt="Sample 1" />
            </SplideSlide>

         </Splide>
      </div>
   </div>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import { defineComponent } from "vue";

export default defineComponent({
   components: {
      Splide,
      SplideSlide,
   },

   setup() {
      const options = {
         rewind: true,
         gap: "1rem",
         autoplay: true,
      };

      return { options };
   },
});
</script>

<style scoped>
.splide__slide img {
   width: 100%;
   height: 300px;
   object-fit: cover; /* Bao phủ toàn bộ khung hình */
   display: block;
}
.content {
   margin-top: 5px;
   position: absolute; /* Để đưa nội dung vào trong khung ảnh */
   right: 10px;
   bottom: 20px;
   width: 400px;
   text-align: justify;
   background-color: #333;
   padding: 7px 7px 12px;
   border-radius: 3px;
   opacity: 0.85;
}
.content a {
   text-decoration: none;
   color: white;
   display: inline-block;
   line-height: 24px;
   text-transform: uppercase;
}
</style>
