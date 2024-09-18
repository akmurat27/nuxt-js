<template>
    <div>
        <div ref="container" class="keen-slider relative overflow flex justify-between items-center my-12 w-[85%] m-auto mt-[8rem]">
            <!-- Ilkinji surat bilen tekst -->
            <div class="keen-slider__slide  relative w-32 md:w-[20%] h-[251px] flex flex-col items-center">
                <img src="~/assets/bg-img/14.png" class="w-[42px] h-[42px] md:w-auto md:h-auto">
                <div class="flex flex-col items-center">
                    <span class="font-bold text-[12px] md:text-[18px]">
                        In-vehicle traffic enforcement
                    </span>
                    <p class="text-center text-xs w-[124px] lg:text-sm lg:w-[222px]">
                        Automatic detection of violation on reserved bus lanes. The system is installed in regular route vehicle and works fully automatic.
                    </p>
                </div>
            </div>

            <!-- Birinji element -->
            <div class="absolute md:top-1/4 md:left-1/4 transform -translate-x-1/2 -translate-y-1/2 top-[8%] left-[48%]">
                <img src="~/assets/bg-img/Vector 3.png" class="md:w-[165px] w-[95px]">
            </div>

            <!-- Ikinji surat bilen tekst -->
            <div class="keen-slider__slide  relative w-32 md:w-[20%] h-[251px] flex flex-col items-center">
                <img src="~/assets/bg-img/4.png" class="w-[42px] h-[42px] md:w-auto md:h-auto">
                <div class="flex flex-col items-center">
                <span class="font-bold text-[12px] md:text-[18px]">
                    Speed and traffic enforcement
                </span>
                <p class="text-center text-[12px] w-[150px] lg:text-sm lg:w-[280px]">
                    Automatic detection of various traffic violations and transfer data to back office. Control speeds of both oncoming and outgoing vehicles in up to four lanes. Onboard automatic number plate recognition (ANPR), evidence collection and data storage.
                </p>
                </div>
            </div>

            <!-- Ikinji element -->
            <div class="hidden md:block absolute md:top-1/4 md:left-1/2 transform -translate-x-1/2 -translate-y-1/2 top-[8%] left-[83%]">
                <img src="~/assets/bg-img/Vector 3.png" class="lg:w-[165px] w-[95px]">
            </div>

            <!-- Üçünji surat bilen tekst -->
            <div class="keen-slider__slide relative w-32 md:w-[20%] h-[251px] flex flex-col items-center">
                <img src="~/assets/bg-img/13.png" class="w-[42px] h-[42px] md:w-auto md:h-auto">
                <div class="flex flex-col items-center">
                <span class="font-bold text-[12px] md:text-[18px]">Portable speed enforcement</span>
                <p class="text-center text-xs lg:text-sm lg:w-[222px]">Hand-held or tripod-based devices for speed measurement and violation evidence collection.</p>
                </div>
            </div>

            <!-- Üçünji element -->
            <div class="hidden md:block absolute md:top-1/4 md:left-3/4 transform -translate-x-1/2 -translate-y-1/2 top-[8%] left-[95%]">
                <img src="~/assets/bg-img/Vector 3.png" class="lg:w-[165px] w-[95px]">
            </div>

            <!-- Dördünji surat bilen tekst -->
            <div class="keen-slider__slide relative w-32 md:w-[20%] h-[251px] flex flex-col items-center">
                <img src="~/assets/bg-img/23.png" class="w-[42px] h-[42px] md:w-auto md:h-auto">
                <div class="flex flex-col items-center">
                <span class="font-bold text-[12px] md:text-[18px]">GRG cameras</span>
                <p class="text-center text-xs lg:text-sm lg:w-[222px]">
                    Low-cost solution for automatic number plate recognition (ANPR) and real time data transfer. Video surveillance and automatic vehicle classification.
                </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { useKeenSlider } from 'keen-slider/vue.es'
import 'keen-slider/keen-slider.min.css'

export default {
    setup(){
    const [container] = useKeenSlider({
        breakpoints: {
        '(min-width: 200px)': {
            slides: { perView: 2, spacing: 1 },
        },
        '(min-width: 1000px)': {
            slides: { perView: 4, spacing: 1 },
        },
        },
        slides: { perView: 1 },
    })
    return { container }
    }
}
</script>

<style scoped>
body {
     margin: 0;
     font-family: 'Inter', sans-serif;
     -webkit-font-smoothing: antialiased;
     -moz-osx-font-smoothing: grayscale;
   }
   [class^="number-slide"],
   [class*=" number-slide"] {
     background: grey;
     display: flex;
     align-items: center;
     justify-content: center;
     font-size: 50px;
     color: #fff;
     font-weight: 500;
     height: 300px;
     max-height: 100vh;
   }
   
   .number-slide1 {
     background: rgb(64, 175, 255);
     background: linear-gradient(
       128deg,
       rgba(64, 175, 255, 1) 0%,
       rgba(63, 97, 255, 1) 100%
     );
   }
   
   .number-slide2 {
     background: rgb(255, 75, 64);
     background: linear-gradient(
       128deg,
       rgba(255, 154, 63, 1) 0%,
       rgba(255, 75, 64, 1) 100%
     );
   }
   
   .number-slide3 {
     background: rgb(182, 255, 64);
     background: linear-gradient(
       128deg,
       rgba(182, 255, 64, 1) 0%,
       rgba(63, 255, 71, 1) 100%
     );
     background: linear-gradient(
       128deg,
       rgba(189, 255, 83, 1) 0%,
       rgba(43, 250, 82, 1) 100%
     );
   }
   
   .number-slide4 {
     background: rgb(64, 255, 242);
     background: linear-gradient(
       128deg,
       rgba(64, 255, 242, 1) 0%,
       rgba(63, 188, 255, 1) 100%
     );
   }

</style>