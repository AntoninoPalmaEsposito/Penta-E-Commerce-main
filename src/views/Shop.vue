<script>
import Slider from '@/components/Slider.vue'

import jsonProducts from '@/assets/products.json'

export default {
    components: {
        Slider
    },
    data() {
        return {
            products: [],
            dis: true,
            cis: true,
            ordinaV: false,
            ordinaCC: false
        }
    },
    mounted() {
        this.products = jsonProducts

    },
    methods: {
        ordinaC() {
            this.ordinaCC = !this.ordinaCC


        },




        ordina() {
            this.ordinaV = !this.ordinaV
        },



        attivaDec() {
            this.cis = true
            this.dis = !this.dis

            if (this.dis === false) {
                this.products.sort((a, b) => a.price - b.price)
            } else {
                window.location.reload();
            }


        },
        attivaCre() {
            this.dis = true
            this.cis = !this.cis

            if (this.cis === false) {
                this.products.sort((a, b) => b.price - a.price)
            } else {
                window.location.reload();
            }

        },
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


<template>
    <h2 class="text-medio lg:text-grande text-center font-bold lg:py-[40px] py-[15px]"> TUTTI I PRODOTTI </h2>

    <div class="flex justify-center md:justify-start w-screen px-auto">

        <!-- Ordina per prezzo -->
        <div class="relative">
            <div @click="ordina"
                class=" flex justify-center items-center p-[5px] border-[2px] w-[130px] border-black text-center text-[18px] ml-0 md:ml-[40px]">
                Prezzo <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512" class="h-[15px] mt-[0px] ml-[7px]">
                    <path
                        d="M169.4 470.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 370.8 224 64c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 306.7L54.6 265.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z" />
                </svg></div>

            <div v-if="ordinaV"
                class="absolute top-[41px] z-10 flex flex-col justify-center items-start px-[20px] bg-slate-400 w-[130px] ml-0 md:ml-[40px] ">

                <div @click="attivaDec" class="pt-[15px]">
                    <button class="text-white hover:underline underline-offset-4">Crescente</button>
                </div>


                <div @click="attivaCre" class="pb-[15px]">
                    <button class="text-white hover:underline underline-offset-4">Decrescente</button>
                </div>

            </div>
        </div>

        <!-- Ordina per categoria -->
        <div class="relative">
            <div @click="ordinaC"
                class="flex justify-center items-center p-[5px] border-[2px] w-[160px] border-black text-center text-[18px] ml-[40px]">
                Categorie <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"
                    class="h-[15px] mt-[0px] ml-[7px]">
                    <path
                        d="M169.4 470.6c12.5 12.5 32.8 12.5 45.3 0l160-160c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L224 370.8 224 64c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 306.7L54.6 265.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l160 160z" />
                </svg></div>

            <div v-if="ordinaCC"
                class="absolute z-10 top-[41px] flex flex-col py-[15px] justify-center items-start px-[20px] bg-slate-400 w-[160px] ml-[40px]">

                <!-- Routerlink -->
                <RouterLink to="/gaming" class="text-white hover:underline underline-offset-4">Gaming</RouterLink>
                <RouterLink to="/elettronica" class="text-white hover:underline underline-offset-4">Elettronica
                </RouterLink>
                <RouterLink to="/casa" class="text-white hover:underline underline-offset-4">Casa</RouterLink>
                <RouterLink to="/fotografia" class="text-white hover:underline underline-offset-4">Fotografia
                </RouterLink>
                <RouterLink to="/elettrodomestici" class="text-white hover:underline underline-offset-4">
                    Elettrodomestici</RouterLink>

            </div>
        </div>
    </div>





    <div class="grid grid-cols-2 lg:grid-cols-4 h-[100%] mt-[20px] ">
        <!-- TUTTI PRODOTTI -->


        <div v-if="dis || cis" v-for="product in products"
            class="flex flex-col justify-center items-center p-[20px] border-[1px] border-gray-100">

            <Slider class="w-[150px] lg:w-[300px] my-auto" :item="product"></Slider>
            <span class="flex flex-col justify-start">
                <h2 class="text-[14px] lg:text-[24px] font-medium ">{{ product.title }}</h2>
                <h2 class="font-medium text-[18px]">{{ product.price }} €</h2>
            </span>

        </div>


        <div v-else v-for="product in products"
            class="flex flex-col justify-center items-center p-[20px] border-[1px] border-gray-100">

            <Slider class="w-[150px] lg:w-[300px] my-auto" :item="product"></Slider>
            <span class="flex flex-col justify-start">
                <h2 class="text-[14px] lg:text-[24px] font-medium ">{{ product.title }}</h2>
                <h2 class="font-medium text-[18px]">{{ product.price }} €</h2>
            </span>

        </div>





    </div>


</template>





<style></style>