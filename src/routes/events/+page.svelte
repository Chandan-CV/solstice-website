<script>
  // @ts-nocheck
  
    import BgAnim from '$lib/common/BGAnim.svelte';
import EventTile from '$lib/events_pg/EventTile.svelte';
    // import { Container } from 'postcss';
    // import { each, onMount } from 'svelte/internal';
        
  
        // let particles = 300
        // let m = {x: 0,y:0}
        // let multiplier = -10
        
        // function newanimate(){
          
        //   var root = document.querySelector(':root');
        //   root.style.setProperty('--x', `${Math.random()*window.innerWidth}%`);
        //   root.style.setProperty('--y', `${Math.random()*window.innerHeight}%`);
        // }
        
      //   function handleMouse(event){
      //     m.x = multiplier*event.clientX;
      //     m.y = multiplier*event.clientY;
      //     var root = document.querySelector(':root');
      //     root.style.setProperty('--x', `${m.x}%`);
      //     root.style.setProperty('--y', `${m.y}%`);
      //   }
      // onMount(()=>{
      //   var countainer = document.getElementById("stars")
      //   for(let i =0;i<particles;i++)
      //   countainer.innerHTML += `<div class=" bg-white h-[3px] w-[3px] rounded-full blur-[1px] absolute ease-in-out s-N-9Ekhs3dG6k" style="top: ${Math.random()*window.innerHeight*1.5}px;left: ${Math.random()*innerWidth*1.5}px;opacity:${Math.random()}" id="star"></div>`
      // })
  
  
       export let data;
  </script>
  <div>
    <!-- <div class="stars  h-full fixed -z-10 w-full stars" id="stars">
      <div class="bg-white h-1 w-1 rounded-full blur-[2px] absolute" style="top: 90px;left:90px" id="star"></div>
    </div> -->
    <div  class=" flex flex-col max-sm:p-10 max-md:p-16 md:p-20 w-screen">
      <BgAnim />
      <h1 class="text-6xl mb-4 font-bold bg-gradient-to-tr  from-[#3BACC1] via-[#2D6DB1] to-[#3BACC1] text-transparent w-fit bg-clip-text">
        Events
      </h1>
      <div class="flex flex-row flex-wrap justify-center items-center">
        {#each data.events as event}
        {#if !event.hide}
          <EventTile data={event}/>
        {/if}
        {/each}
      </div>
    </div>
    
  </div>
  
  
  <style>
  /* :root{
    --x : 100%;
    --y : 100%;
  } */
  
  /* .stars div{
    transform: translate(var(--x),var(--y));
  } */
  </style>
  
