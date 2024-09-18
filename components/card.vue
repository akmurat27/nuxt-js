<template>
    <div>
        <div class="flex flex-col lg:flex-row items-center justify-between md:w-[90%] m-auto" style="margin-top: 5rem;">
            <div class="relative trophy h-[220px] md:h-[410px] md:w-[420px] p-5">
                <h1 class="text-white font-normal text-[22px] md:text-[32px]">Metal önümçiliginiň geljegi: innowasiýa we durnuklylyk:</h1>
                <p class="text-white text-[14px] md:text-[20px] absolute">
                    Metal häzirki zaman dünýäsini döredýär: Metal önümçiligi durmuşymyza nähili täsir edýär: Bu mowzuk metal önümçiliginiň gündelik durmuşymyzda möhüm ähmiýete eýe. Binalardan, transportdan başlap, elektronika we lukmançylyk enjamlaryna çenli metallaryň nähili ulanylýandygyny görkezip biler.
                </p>
                <div class="absolute left-[70%] bottom-[1px]">
                    <img src="~/assets/trophy/trophy.png">
                </div>
            </div>
            <div class="border shadow-lg flex p-4 items-center justify-center mt-5 md:mt-0 h-[261px] md:h-[410px] md:w-[790px]">
                <div class="flex flex-col md:w-[400px] items-end">
                    <div class="flex items-center h-[110px] border-r-2 border-b-2">
                        <h1 class="text-sm md:text-2xl md:font-bold">20+ <br>
                            Products</h1>
                        <img src="~/assets/trophy/box-2.png" class="mr-[6rem] ml-5">
                    </div>
                    <div class="flex items-center h-[110px] border-t-2 border-r-2">
                        <h1 class="text-sm md:text-2xl md:font-bold">80 <br>
                            Successful Projects</h1>
                        <img src="~/assets/trophy/award.png" class="mx-4">
                    </div>
                </div>

                <div class="flex flex-col  md:w-[400px] items-start">
                    <div class="flex items-center h-[110px] border-l-2 border-b-2">
                        <h1 class="text-sm md:text-2xl md:font-bold ml-[3rem] mr-2">1561 <br>
                        End-User Instutions</h1>
                        <img src="~/assets/trophy/courthouse.png">
                    </div>
                    <div class="flex items-center h-[110px] border-t-2 border-l-2">
                        <h1 class="text-sm md:text-2xl md:font-bold ml-[3rem] mr-2">4618 <br>
                        System Working 24/7</h1>
                        <img src="~/assets/trophy/setting-2.png">
                    </div>
                </div>
            </div>
        </div>    
    </div>
</template>


<style scoped>
.trophy{
    background-color: #002855;
}
.container {
  display: flex;
  flex-wrap: wrap; /* Allows items to wrap onto multiple lines */
  gap: 10px; /* Adds space between items */
  width: 70%;
  align-items: flex-start;
  padding-top: 16px;
}

.item {
  flex: 1 1 calc(50% - 20px); /* Adjusts item width, accounting for the gap */
  padding-top: 10px;
  padding-right: 10px;
}
</style>