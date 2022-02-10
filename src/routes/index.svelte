<svelte:head>
    <title>Home</title>
</svelte:head>

<script lang="ts">
import {
    Navigation,
    Autoplay
} from "swiper"
import {
    Swiper,
    SwiperSlide
} from "swiper/svelte";
import "swiper/css"
import "swiper/css/navigation"
interface SliderContentInterface {
    headText: string;
    subtext: string;
    img: string;
    link: {
        href: string;
        text: string;
    }
};
const sliderContent: SliderContentInterface[] = [{
        headText: "explore, discover, travel",
        subtext: "travel arround the world",
        img: "images/home-slide-1.jpg",
        link: {
            href: "/package",
            text: "discover more"
        }
    },
    {
        headText: "explore, discover, travel",
        subtext: "travel arround the world",
        img: "images/home-slide-2.jpg",
        link: {
            href: "/package",
            text: "discover more"
        }
    },
    {
        headText: "explore, discover, travel",
        subtext: "travel arround the world",
        img: "images/home-slide-3.jpg",
        link: {
            href: "/package",
            text: "discover more"
        }
    }
];
</script>

<!-- home section starts  -->

<section class="home">

    <div class="swiper home-slider">
 
       <!-- <div class="swiper-wrapper"> -->
          <Swiper
          loop="{true}"
          autoplay="{true}"
          modules="{[Navigation, Autoplay]}"
          navigation="{{
             nextEl: ".swiper-button-next",
             prevEl: ".swiper-button-prev",
          }}"
          >
      
 
          {#each sliderContent as {headText, img, link, subtext}}
            <SwiperSlide>
               <div class="slide" style="background:url(/{img}) no-repeat">
                  <div class="content">
                  <span>{headText}</span>
                  <h3>{subtext}</h3>
                  <a href="{link.href}" class="btn">{link.text}</a>
                  </div>
              </div>
            </SwiperSlide>
          {/each}
          
       <!-- </div> -->
       </Swiper>
 
       <div class="swiper-button-next"></div>
       <div class="swiper-button-prev"></div>
 
    <!-- </div> -->

 
 </section>
 
 <!-- home section ends -->

 <!-- services section starts  -->

<section class="services">

    <h1 class="heading-title"> our services </h1>
 
    <div class="box-container">
 
       <div class="box">
          <img src="images/icon-1.png" alt="">
          <h3>adventure</h3>
       </div>
 
       <div class="box">
          <img src="images/icon-2.png" alt="">
          <h3>tour guide</h3>
       </div>
 
       <div class="box">
          <img src="images/icon-3.png" alt="">
          <h3>trekking</h3>
       </div>
 
       <div class="box">
          <img src="images/icon-4.png" alt="">
          <h3>camp fire</h3>
       </div>
 
       <div class="box">
          <img src="images/icon-5.png" alt="">
          <h3>off road</h3>
       </div>
 
       <div class="box">
          <img src="images/icon-6.png" alt="">
          <h3>camping</h3>
       </div>
 
    </div>
 
 </section>
 
 <!-- services section ends -->
 
 <!-- home about section starts  -->
 
 <section class="home-about">
 
    <div class="image">
       <img src="images/about-img.jpg" alt="">
    </div>
 
    <div class="content">
       <h3>about us</h3>
       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita et, recusandae nobis fugit modi quibusdam ea assumenda, nulla quisquam repellat rem aliquid sequi maxime sapiente autem ipsum? Nobis, provident voluptate?</p>
       <a href="/about" class="btn">read more</a>
    </div>
 
 </section>
 
 <!-- home about section ends -->
 
 <!-- home packages section starts  -->
 
 <section class="home-packages">
 
    <h1 class="heading-title"> our packages </h1>
 
    <div class="box-container">
 
       <div class="box">
          <div class="image">
             <img src="images/img-1.jpg" alt="">
          </div>
          <div class="content">
             <h3>adventure & tour</h3>
             <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos, sint!</p>
             <a href="/book/a very fine location" class="btn">book now</a>
          </div>
       </div>
 
       <div class="box">
          <div class="image">
             <img src="images/img-2.jpg" alt="">
          </div>
          <div class="content">
             <h3>adventure & tour</h3>
             <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos, sint!</p>
             <a href="/book/a very fine location" class="btn">book now</a>
          </div>
       </div>
       
       <div class="box">
          <div class="image">
             <img src="images/img-3.jpg" alt="">
          </div>
          <div class="content">
             <h3>adventure & tour</h3>
             <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eos, sint!</p>
             <a href="/book/a very fine location" class="btn">book now</a>
          </div>
       </div>
 
    </div>
 
    <div class="load-more"> <a href="/package" class="btn">load more</a> </div>
 
 </section>
 
 <!-- home packages section ends -->
 
 <!-- home offer section starts  -->
 
 <section class="home-offer">
    <div class="content">
       <h3>upto 50% off</h3>
       <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure tempora assumenda, debitis aliquid nesciunt maiores quas! Magni cumque quaerat saepe!</p>
       <a href="/book" class="btn">book now</a>
    </div>
 </section>
 
 <!-- home offer section ends -->
