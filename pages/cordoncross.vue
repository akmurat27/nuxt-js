<template>
    <div>
        <div class="hidden md:flex items-center w-[85%] m-auto py-5">
            <nuxt-link
                    to="/"
                    :class="{ active: isActive('/') }"
                    class="underline"
                >
                    Home
                </nuxt-link>
            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
            <nuxt-link
                    to="/product"
                    :class="{ active: isActive('/product') }"
                    class="underline"
                >
                    Products
                </nuxt-link>
            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
            <h1 class="underline">Speed and traffic enforcement </h1>
            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
            <nuxt-link
                to="/cordoncross"
                :class="{ active: isActive('/cordoncross') }"
            >
                «CORDON-CROSS»
            </nuxt-link>
        </div>
        <div class="w-[85%] m-auto md:flex mt-8">
            <img src="~/assets/product/CORDON-TEMP_with_background-300x271 (4).png">
            <div class="flex flex-col md:w-[523px] m-auto">
                <h1 class="text-[22px] text-blue-800 md:text-[48px] mb-10 mt-4 md:mt-0">«CORDON-CROSS»</h1>
                <h1 class="md:text-[28px] font-medium">RAFFIC ENFORCEMENT SYSTEM</h1>
                <div class="w-[260px] h-[5px] bg-blue-800 my-4"></div>
                <p>
                    The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.The “CORDON-CROSS” stationary system is designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office.
                </p>
            </div>
        </div>
        <div class="w-[85%] m-auto">
            <h1 class="text-[22px] md:text-[48px] font-bold my-4">металлопрокат завод фото</h1>
            <div v-for="(card, i) in cards" :key="i" class="border border-1px bg-grey-500 rounded-[44px] p-6 my-4 md:flex">
                <img src='~/assets/product/CORDONTEMPwithbackground300x271.png'>
                <div class="hidden md:flex flex-col justify-between h-[324px] w-[820px] m-auto">
                    <div class="hidden md:block text-[30px] font-bold">{{ card.text }}</div>
                    <div class="hidden md:block text-[20px]">{{ card.par }}</div>
                    <div class="hidden md:block bg-blue-800 text-[20px] p-2 w-[142px] h-[50px] rounded-[10px] text-white text-center">{{ card.button }}</div>
                </div>
            </div>
        </div>
        <div class="w-[85%] m-auto mt-5 md:hidden">
            <h1 class="text-[22px] font-bold md:text-[42px]">ADVERTISING AND MARKETING MATERIALS</h1>
            <div class="w-[144px] md:w-[240px] h-[5px] bg-blue-800 my-4"></div>
            <p>Company advertising booklet.</p>
            <div class="w-[165px] md:w-[285px] my-5 rounded-[10px] h-[50px] bg-blue-800 flex items-center justify-center">
                <img src="~/assets/product/download.svg">
                <h1 class="text-white mx-3">Download</h1>
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
                // img: '~/assets/product/CORDONTEMPwithbackground300x271.png',
                text: '«CORDON-CROSS» TRAFFIC ENFORCEMENT SYSTEM FOR INTERSECTIONS',
                par: 'New generation of stationary systems designed for monitoring and photo-video recording of traffic violations at road intersections with data transmission to Police back-office. At the crossroads, all units of the system are connected using fiber-optic communication lines.',
                button: 'Read more'
            },
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