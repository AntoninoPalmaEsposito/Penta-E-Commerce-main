<template>
    <div class="relative">
        <!-- Icona carrello -->
        <div class="mr-[5vw] md:mr-[20px] w-[8.5vw] md:w-[35px]">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
                <path
                    d="M0 24C0 10.7 10.7 0 24 0H69.5c22 0 41.5 12.8 50.6 32h411c26.3 0 45.5 25 38.6 50.4l-41 152.3c-8.5 31.4-37 53.3-69.5 53.3H170.7l5.4 28.5c2.2 11.3 12.1 19.5 23.6 19.5H488c13.3 0 24 10.7 24 24s-10.7 24-24 24H199.7c-34.6 0-64.3-24.6-70.7-58.5L77.4 54.5c-.7-3.8-4-6.5-7.9-6.5H24C10.7 48 0 37.3 0 24zM128 464a48 48 0 1 1 96 0 48 48 0 1 1 -96 0zm336-48a48 48 0 1 1 0 96 48 48 0 1 1 0-96z" />
            </svg>
        </div>

        <!-- Notifica carrello -->
        <div v-if="cartMessage"
            class="bg-red-500 text-white font-bold text-[2.3vw] md:text-[12px] p-[0.8vw] md:p-1 leading-none w-[4vw] md:w-[20px] h-[4vw] md:h-[20px] flex items-center justify-center rounded-full absolute top-[-3.5vw] md:top-[-15px] right-[1.5vw] md:right-[-5px]">
            {{ cartMessage > 99 ? "99+" : cartMessage }}
        </div>
    </div>
</template>

<script>
import { mapStores } from 'pinia';
import { useCartStore } from '@/stores/cart';

export default {
    data() {
        return {
            cartMessage: 0
        }
    },
    computed: {
        ...mapStores(useCartStore)
    },
    mounted() {
        this.updateCart()
        this.cartStore.$subscribe(() => {
            this.cartMessage = 0
            this.updateCart()
        })
    },
    methods: {
        updateCart() {
            this.cartStore.items.forEach(item => {
                this.cartMessage += item.quantity;
            })
        }
    }
}


</script>