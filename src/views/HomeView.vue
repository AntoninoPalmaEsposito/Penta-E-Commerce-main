<template>



  <!-- tutti i prodotti -->
  <div class="relative md:block">
    <div class="absolute md:hidden top-0 w-screen h-[85vh] bg-gradient-to-b from-black to-[rgba(0,0,0,0)]" ></div>
    
  <section class="bg-cover bg-no-repeat lg:bg-top h-[85vh] lg:h-[80vh] p-0 md:p-[20px] bg-slate-300 flex flex-col justify-between md:justify-start   items-center bg-[url('../../src/assets/img/telefonia3.png')]">

    <div class="z-10">
    <h1 class="text-[9vw] md:text-[45px] xl:text-[55px] mt-[15vw] md:mt-0 leading-[11vw] md:leading-[100px] xl:leading-[130px] text-center text-white md:text-black z-10  font-extrabold mb-[8vw] md:mb-0 px-[5vw] md:px-0">
      Scopri il Futuro della Tecnologia! 
    </h1>

    <p class=" px-[5vw]  leading-[7vw] md:px-[100px] xl:px-[200px] text-center text-white md:text-black z-10 text-[5vw] md:text-[25px] xl:text-[30px] md:leading-[35px] xl:leading-[45px] flex flex-col items-center font-semibold ">Esplora la nostra vasta gamma di prodotti tecnologici, dalle ultime novità in telefonia mobile alle lavatrici intelligenti.  Esplora il nostro negozio e porta a casa tua il futuro oggi stesso!  </p>
  </div>
    

    <RouterLink to="/Shop" class= " w-[170px] z-10 ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mb-[10vw] md:mb-[0px] md:mt-[50px] px-[20px] py-[10px] border-[2px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
  </section>
</div>



  <!-- container prodotti specifici -->
  <section class="px-[10px] mt-[50px]">

    <!-- box gaming-->
    
    <RouterLink to="/gaming" class=" text-white h-[400px] bg-cover bg-center lg:h-[700px] bg-slate-400 flex flex-col justify-end items-start " style="background-image: url('https://images.unsplash.com/photo-1559706690-1311487b0b51?q=80&w=1770&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' )"> 
      <div class="flex w-full h-full flex-col backdrop-brightness-50 hover:backdrop-brightness-100 justify-end lg:p-10 p-4 ease-in-out duration-200">
      <h2 class="text-medioMobile lg:text-grande font-bold lg:mb-6"> Entra nel Mondo del Gaming!  </h2>
      <p class="text-[18px] flex-col  font-medium hidden lg:flex ">
        Scopri la nostra vasta gamma di prodotti gaming, dalle ultime console ai migliori accessori. <span>Clicca qui sotto per immergerti nell'universo del gaming e portare a casa l'esperienza di gioco perfetta oggi stesso!</span>  
      </p>
      <RouterLink to="/gaming" class="w-[170px] ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mt-[20px] lg:mt-[30px] px-[20px] py-[10px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
    </div>
    </RouterLink>
  




    <!-- container 2 -->
    <div class=" sm:gap-4 gap-2 w-full grid lg:grid-cols-2 grid-cols-1 mt-2 sm:mt-4">

      <!--fotografia  -->
      <RouterLink to="/fotografia" class="lg:h-[600px] bg-cover bg-center h-[400px] bg-slate-400 flex justify-end items-start flex-col" style="background-image: url('https://images.unsplash.com/photo-1506241537529-eefea1fbe44d?q=80&w=1770&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' )">
      <div class="flex w-full h-full flex-col backdrop-brightness-50 hover:backdrop-brightness-100 justify-end lg:p-6 p-3 ease-in-out duration-200">
        <h2 class="text-medioMobile text-white lg:text-grande font-semibold"> FOTOGRAFIA </h2>
        <RouterLink to="/fotografia" class=" w-[170px] ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mt-[20px] lg:mt-[30px] px-[20px] py-[10px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
    </div>
      </RouterLink>

      <!-- elettronica -->
      <RouterLink to="/elettronica" class=" lg:h-[600px] bg-cover bg-center h-[400px] bg-slate-400 flex justify-end items-start flex-col" style="background-image: url('https://images.unsplash.com/flagged/photo-1572609239482-d3a83f976aa0?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D' )">
        <div class="flex w-full h-full flex-col backdrop-brightness-50 hover:backdrop-brightness-100 justify-end lg:p-6 p-3 ease-in-out duration-200">
        <h2 class=" text-white text-medioMobile lg:text-grande font-semibold "> ELETTRONICA</h2>
        <RouterLink to="/elettronica" class=" w-[170px] ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mt-[20px] lg:mt-[30px] px-[20px] py-[10px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
    </div>
      </RouterLink>

      <!-- elettrodomestici -->
      <RouterLink to="/elettrodomestici" class="lg:h-[600px] h-[400px] bg-cover bg-center bg-slate-400 flex justify-end items-start flex-col" style="background-image: url('https://img.freepik.com/free-vector/household-appliances-realistic-composition_1284-65307.jpg' )">
        <div class="flex w-full h-full flex-col backdrop-brightness-50 hover:backdrop-brightness-100 justify-end lg:p-6 p-3 ease-in-out duration-200">
        <h2 class=" text-white text-medioMobile lg:text-grande font-semibold "> ELETTRODOMESTICI </h2>
        <RouterLink to="/elettrodomestici" class=" w-[170px] ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mt-[20px] lg:mt-[30px] px-[20px] py-[10px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
  </div>
      </RouterLink>

      <!-- casa -->
      <RouterLink to="/casa" class="lg:h-[600px] h-[400px] bg-cover bg-center bg-slate-400 flex justify-end items-start flex-col" style="background-image: url('https://img.freepik.com/free-photo/empty-modern-room-with-furniture_23-2149178335.jpg' )">
        <div class="flex w-full h-full flex-col backdrop-brightness-50 hover:backdrop-brightness-100 justify-end lg:p-6 p-3 ease-in-out duration-200">
        <h2 class=" text-white text-medioMobile lg:text-grande font-semibold "> CUCINA </h2>
        <RouterLink to="/casa" class=" w-[170px] ease-in-out duration-300 flex justify-center items-center text-white rounded-[10px] bg-blue-600 mt-[20px] lg:mt-[30px] px-[20px] py-[10px] text-piccolo
 hover:bg-white hover:ease-in-out hover:text-black font-semibold ">
      Acquista ora
    </RouterLink>
  </div>
      </RouterLink>

     
    </div>
  </section>

  

</template>

<script>
import { RouterLink } from 'vue-router';

import jsonProducts from '@/assets/products.json'

export default {
  data() {
    return {
      products: []
    }
  },
  mounted() {
    this.products = jsonProducts
    console.log(this.products)
  },
  methods: {
    productsByCategory(category) {
      let resultArray = []

      jsonProducts.forEach(product => {
        if (product.categories.includes(category))
          resultArray.push(product)
      })

      return resultArray;
    }
  }
}

</script>
