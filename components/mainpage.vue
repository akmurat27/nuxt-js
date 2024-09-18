<template>
    <div>
        <div class="flex flex-col-reverse w-[85%] pt-6 m-auto md:flex-row items-center md:items-start md:justify-between">
            <div class="md:w-[612px] md:h-[278px] pt-5 mt-[3rem] md:mt-0">
                <span class="text-[22px] lg:text-4xl pt-3 font-bold tracking-wider">Kompaniýanyň çözgütleri  önümçiligi öndürmek halkymyzyň hyzmatyny ýerine ýetirmekden ybarat bolup durýar.</span>
                <p class="text-[14px] pt-3">Dowamly tejribe ýaly metal öndürmek tehnologiýasyndaky soňky üstünlikleri öwrenýär. Bu täzelikleriň pudagyň geljegini nähili emele getirýändigini ara alyp maslahatlaşyp biler.</p>
            </div>
            <div class="relative">
                <img src="~/assets/bg-img/GROM_with_background-300x283 1.png" class="md:w-[484px] md:h-[457px] md:p-10 p-6 border border-2 rounded-[59px] cursor-pointer" @click="openModal">
                <img src="~/assets/bg-img/Group 48096493.png" class="absolute top-[45%] left-[-7%]">
                <img src="~/assets/bg-img/Group 48096492.png" class="absolute top-[45%] left-[93%]">
                <div 
                    v-if="isModalOpen" 
                    class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50 z-50"
                >
                    <div class="relative">
                        <img src="~/assets/bg-img/GROM_with_background-300x283 1.png" class="md:w-[600px] md:h-[500px]">
                        <button @click="closeModal" class="absolute top-0 left-[82%] mt-4  px-4 py-2 rounded">
                            <img src="~/assets/bg-img/icon.svg">
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false
    };
  },
  methods: {
    openModal() {
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
    }
  }
};
</script>

<style scoped>
/* Add any additional styles here */
</style>