<svelte:head>
    <title>Package</title>
</svelte:head>

<script lang="ts">
import {
    onMount
} from "svelte"
let currentitem: number = 6
let box
let packages = [
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!"
   },
   {
      h3: "adventure & tour",
      opened: false,
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
      opened: false
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
      opened: false
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
      opened: false
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
      opened: false
   },
   {
      h3: "adventure & tour",
      p: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis, perspiciatis!",
      opened: false
   },
]
let loadMorePackage = function() {
      for (let i = currentitem; i < currentitem + 3; i++) {
         if(Object(packages[i]).hasOwnProperty("opened")) {
            packages[i].opened = true
            packages[i] = packages[i]
         }
      }
      currentitem += 3
      packages = packages

}


</script>

<div class="heading" style="background:url(images/header-bg-2.png) no-repeat">
    <h1>packades</h1>
 </div>

 <!-- packages section starts  -->

 <section class="packages">

    <h1 class="heading-title">top destinations</h1>

    <div class="box-container">

       {#each packages as {h3, p, opened},i}
         <div class="box">
            <div class="image">
               <img src="images/img-{i + 1}.jpg" alt="">
            </div>
            <div class="content">
               <h3>{h3}</h3>
               <p>{p}</p>
               <a href="/book/{h3}" class="btn">book now</a>
            </div>
         </div>
         {#if opened}
            <div class="box" style="display: {opened ? "inline-block" : "none"};">
               <div class="image">
                  <img src="images/img-{i + 1}.jpg" alt="">
               </div>
               <div class="content">
                  <h3>{h3}</h3>
                  <p>{p}</p>
                  <a href="/book/{h3}" class="btn">book now</a>
               </div>
            </div>
         {/if}
       {/each}

    </div>

    <div class="load-more" style="display: {currentitem >= packages.length ? "none" : "block"};">
       <span class="btn" on:click="{() => loadMorePackage()}">load more</span>
      </div>

 </section>

 <!-- packages section ends -->
