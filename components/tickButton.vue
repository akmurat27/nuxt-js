<template>
    <div>
        <div class="relative flex mt-[10rem] md:h-[680px] overflow-hidden">
            <div class="bg-pic w-[100%] md:w-[85%]">
                <div class="w-[85%] m-auto pt-4">
                    <h1 class="text-[22px] lg:text-[42px] font-medium md:w-[936px] tracking-wider">Näme üçin Hil holyklyk Jemgyýetini saýlaýarsyňyz?</h1>
                    <p class="md:w-[502px] pt-4">
                        Metal önümçiliginiň haýran galdyryjy dünýäsi: Magdanlardan gündelik zatlara: Bu mowzuk çig maly gazyp almakdan başlap, taýýar önümlere öwürmek ýaly ähli metal önümçiligini öwrenýär. Ulanylan dürli usullary we ajaýyp üýtgeşik metallary görkezip biler.
                    </p>
                    <div class="container">
                        <div class="item flex items-center" v-for="(tick,i) in tickButton" :key="i">
                            <button @click="toggleTick" :class="{ ticked: isTicked }" class="mr-2">
                                <div class="circle">
                                    <span v-if="isTicked">✔️</span>
                                </div>
                            </button>
                            <div class="text-[14px] md:text-[16px]">
                                {{ tick.text }}
                            </div>
                        </div>
                    </div>  
                </div>
            </div>
            <div class="hidden lg:block lg:absolute lg:top-[40%] lg:left-[63%] z-50">
                <img src="~/assets/bg-img/Frame 28.png">
            </div>
            <div class="blue-pic hidden md:block absolute inset-0 left-[60%]">
            </div>
        </div>      
    </div>
  </template>
  
  <script>
  export default {
    data: () => ({
        isTicked: false,
        tickButton:[
        {
            text: "Solution-oriented approach",
        },
        {
            text: "Positive and strong communication.",
        },
        {
            text: "Innovative perspective.",
        },    
        {
            text: "Proven solutions.",
        },    
        {
            text: "Expert and experienced staff.",
        },    
        {
            text: "Not just a supplier; but a solution partner.",
        },    
        {
            text: "Dynamic team, fast reaction.",
        },    
        {
            text: "Cares about end-user requests.",
        },           
        {
            text: "Always the latest technology.",
        },           
        {
            text: "Certified products.",
        },            
        {
            text: "Loyal to the plan and dates.",
        },           
        {
            text: "Effective after-sales support.",
        }        
    ]
    }),
    methods: {
      toggleTick() {
        this.isTicked = !this.isTicked;
      }
    }
  }
  </script>
  
  <style scoped>
  .bg-pic{
    background-color: #EEF6FF;
  }
  .blue-pic{
    background-color: #002855;
    width: 619px;
    height: auto;
    clip-path: polygon(50% 0%,100% 0%,100% 100%,0% 100%);
    
  }
  button {
    background: none;
    border: none;
    cursor: pointer;
    padding: 0;
  }
  
  .circle {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background-color: #EEF6FF;
    border: 2px solid #002855; /* Border color when not ticked */
    font-size: 24px;
    color: transparent;
  }
  
  .ticked .circle {
    background-color: green;
    color: white;
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
/* Adjust layout for smaller screens */
@media (max-width: 768px) {
  .item {
    flex: 1 1 calc(50% - 20px); /* 2 items per row */
  }
}

@media (max-width: 480px) {
  .item {
    flex: 1 1 calc(100% - 20px); /* 1 item per row */
  }
}
  </style>
  