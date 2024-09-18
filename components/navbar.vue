<template>
    <div class="shadow-md">
        <div class="flex w-full h-[44px]" style="background-color: #002855;">
                <div class="w-[85%] flex items-center justify-end lg:flex lg:justify-end m-auto " >
                    <div class="flex text-white w-[100%] justify-center lg:w-auto">
                        <img src="~/assets/nav-icons/call-calling.svg" class="mx-2">
                        <span>+993 64 92 93 40</span>
                    </div>
                    <div>
                        <img src="~/assets/nav-img/Rectangle 2 (1).png" class="mx-6 hidden lg:block">
                    </div>
                <div class="flex text-white">
                    <img src="~/assets/nav-icons/sms.svg" class="mx-2 hidden lg:block">
                    <span class="hidden lg:block">rowsenart@gmail.com</span>
                </div>
                <div>
                    <img src="~/assets/nav-img/Rectangle 2 (1).png" class="mx-6 hidden lg:block">
                </div>
                <div class="relative flex text-white cursor-pointer" @mouseenter="modalOpen" @mouseleave="modalClose">
                    <img src="~/assets/nav-img/Flag_of_Turkmenistan.png" class="w-[33px] h-[22px] mx-2">
                    <span class="hidden lg:block">Turkmen</span>

                    <!-- Modal (v-show to toggle visibility without re-rendering) -->
                    <div
                        v-show="isOpenModal"
                        class="hidden md:block absolute top-0 left-0 mt-12 bg-white border-2 rounded-[16px] z-50 w-[180px] h-[115px]"
                    >
                        <div class="flex items-center justify-center russkiy p-2 rounded-lg w-[144px] m-auto mt-3 h-[36px]">
                            <img src="~/assets/nav-icons/Rectangle 18 (2).png">
                            <h2 class="text-lg font-semibold text-black">Русский</h2>
                        </div>
                        <div class="flex items-center justify-center">
                            <img src="~/assets/nav-icons/Rectangle 17.png">
                            <h2 class="text-lg font-semibold text-black">English</h2>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="w-[85%] m-auto flex items-center justify-between">
            <img src="~/assets/nav-img/Group 48096510.png" class="mt-[20px]">
            <img src="~/assets/nav-icons/menu-05.svg" class="lg:hidden cursor-pointer" @click="openModal">
            <div 
                v-if="isModalOpen" 
                class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"
            >
                <div class="bg-white w-full h-[520px]">
                    <div class="flex items-center justify-between p-4">
                        <h1 class="text-[28px] font-bold">Hil hojalyk jemgyyeti</h1>
                        <button @click="closeModal" class="mt-4 px-4 py-2 links rounded-[12px]">
                            <img src="~/assets/bg-img/icon.svg">
                        </button>
                    </div>
                    <div class="flex flex-col p-4">
                        <nuxt-link
                            to="/"
                            class="links  text-[22px] p-4 flex items-center justify-between w-full rounded-[12px] h-[50px] text-[22px] tracking-wider my-2"
                        >
                            Home
                            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
                        </nuxt-link>
                        <nuxt-link
                            to="/product"
                            class="links text-[22px] p-4 flex items-center justify-between w-full rounded-[12px] h-[50px] text-[22px] tracking-wider my-2"
                        >
                            Product
                            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
                        </nuxt-link>
                        <nuxt-link
                            to="/contact"
                            class="links text-[22px] p-4 flex items-center justify-between w-full rounded-[12px] h-[50px] text-[22px] tracking-wider my-2"
                        >
                            Contact
                            <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
                        </nuxt-link>
                    </div>
                    <div class="w-[130px] m-auto mt-[5rem]">
                        <img src="~/assets/nav-img/Group 48096510 (1).png">
                    </div>
                </div>
            </div>
            <div class="flex w-[20%] items-center justify-evenly hidden lg:block lg:flex">
                <nuxt-link
                    to="/"
                    :class="{ active: isActive('/') }"
                >
                    Home
                </nuxt-link>
                <nuxt-link
                    to="/product"
                    :class="{ active: isActive('/product') }"
                >
                   Product
                </nuxt-link>
                <nuxt-link
                    to="/contact"
                    :class="{ active: isActive('/contact') }"
                >
                    Contact
                </nuxt-link>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isModalOpen: false,
            isOpenModal: false
        };
    },
  methods: {
    isActive(route) {
      return this.$route.path === route;
    },
    openModal() {
      this.isModalOpen = true;
    },
    modalOpen() {
        this.isOpenModal = true;
    },
    closeModal() {
      this.isModalOpen = false;
    },
    modalClose() {
        this.isOpenModal = false;
    }
  }
}
</script>

<style scoped>
.active {
  color: rgb(255, 255, 255);
  padding: 15px;
  background-color: #002855;
  border-radius: 10px;
}
.links{
    background-color: #F5F5F5;
}
.russkiy{
    background-color: #AFAFAF;
}
</style>

