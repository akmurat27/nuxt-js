<template>
    <div>
        <div class="mt-[20px]">
            <img src="~/assets/product/H30aba39c30984aafbe9b9905d33f2482e 1.png" class="w-full h-[153px] md:h-auto">
            <div class="absolute md:top-[35%] md:left-[20%] top-[16%] left-[8%] flex flex-col items-center justify-center">
                <h1 class="text-[22px] md:text-[42px] text-white font-bold">PRODUCTS</h1>
                <p class="text-[16px] md:text-[22px] text-white text-center w-[343px] md:w-[900px]">The company produces and offers a wide range of automatic traffic enforcement equipment, photo radar systems and intelligent road cameras.</p>
            </div>
            <div class="flex items-center w-[85%] m-auto mt-4">
                <nuxt-link
                    to="/"
                    :class="{ active: isActive('/') }"
                >
                    Home
                </nuxt-link>
                <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
                <nuxt-link
                    to="/product"
                    :class="{ active: isActive('/product') }"
                >
                   Product
                </nuxt-link>
            </div>
            <div class="w-[85%] m-auto">
                <h1 class="text-[22px] md:text-[48px] my-5">Bizin eden onumlerimiz barada tanysmak </h1>
                <div class="w-[240px] h-[5px] bg-blue-500"></div>
                <p class="mt-3">Выбор металлопроката: производство и характеристикВыбор металлопроката: производство и характеристикВыбор металлопроката: производство и характеристикВыбор металлопроката: производство и характеристик</p>
            </div>
            <nuxt-link to="/cordoncross">
                <div class="w-[85%] m-auto">
                    <div v-for="(card,i) in cards" :key="i" class="border border-1px bg-grey-500 rounded-[44px] p-6 my-4 md:flex">
                        <img src='~/assets/product/CORDONTEMPwithbackground300x271.png'>
                        <div class="hidden md:flex flex-col justify-between h-[324px] w-[820px] m-auto">
                            <div class="hidden md:block text-[30px] font-bold">{{ card.text }}</div>
                            <div class="hidden md:block text-[20px]">{{ card.par }}</div>
                            <div class="hidden md:block bg-blue-800 text-[20px] p-2 w-[142px] h-[50px] rounded-[10px] text-white text-center">{{ card.button }}</div>
                        </div>
                    </div>
                </div>
            </nuxt-link>
            <div class="border border-[1px] rounded-[8px] bg-grey-500 flex justify-evenly items-center w-[300px] h-[40px] m-auto">
                <h1 class="text-blue-800">Previous</h1>
                <div>
                    <span class="text-blue-800 border border-[1px] bg-grey-500 p-2">1</span>
                    <span class="text-white bg-blue-800 border border-[1px] bg-grey-500 p-2">2</span>
                    <span class="text-blue-800 border border-[1px] bg-grey-500 p-2">3</span>
                </div>
                <h1 class="text-blue-800">Next</h1>
            </div>
            <div class="w-[85%] m-auto mt-5">
                <h1 class="text-[22px] font-bold md:text-[42px]">ADVERTISING AND MARKETING MATERIALS</h1>
                <div class="w-[144px] md:w-[240px] h-[5px] bg-blue-800 my-4"></div>
                <p>Company advertising booklet.</p>
                <div class="w-[165px] md:w-[285px] my-5 rounded-[10px] h-[50px] bg-blue-800 flex items-center justify-center">
                    <img src="~/assets/product/download.svg">
                    <h1 class="text-white mx-3">Download</h1>
                </div>
            </div>
        </div>
    </div>
</template>
  
<script>
export default {
    data: () => ({
        cards: [
            {
                // img: '~/assets/product/CORDONTEMPwithbackground300x271.png',
                text: '«CORDON-CROSS» TRAFFIC ENFORCEMENT SYSTEM FOR INTERSECTIONS',
                par: 'New generation of stationary systems designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office. At the crossroads, all units of the system are connected using fiber-optic communication lines.',
                button: 'Read more'
            },
            {
                // img: '~/assets/product/CORDON-TEMP_with_background-300x271.png',
                text: '«CORDON-CROSS» TRAFFIC ENFORCEMENT SYSTEM FOR INTERSECTIONS',
                par: 'New generation of stationary systems designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office. At the crossroads, all units of the system are connected using fiber-optic communication lines.',
                button: 'Read more'
            },
            {
                // img: '~/assets/product/CORDON-TEMP_with_background-300x271.png',
                text: '«CORDON-CROSS» TRAFFIC ENFORCEMENT SYSTEM FOR INTERSECTIONS',
                par: 'New generation of stationary systems designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office. At the crossroads, all units of the system are connected using fiber-optic communication lines.',
                button: 'Read more'
            },
            {
                // img: '~/assets/product/CORDON-TEMPx_with_background-300x271.png',
                text: '«CORDON-CROSS» TRAFFIC ENFORCEMENT SYSTEM FOR INTERSECTIONS',
                par: 'New generation of stationary systems designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office. At the crossroads, all units of the system are connected using fiber-optic communication lines.',
                button: 'Read more'
            }
        ]
    }),
    methods: {
        isActive(route) {
        return this.$route.path === route;
        }
    }
}
</script>

<style>
.active {
    font-weight: bold;
}
</style>
  