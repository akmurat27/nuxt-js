<template>
    <div>
        <div class="mt-4">
            <img src="~/assets/contact/H30aba39c30984aafbe9b9905d33f2482e 1 (1).png" class="w-full h-[153px] md:h-auto">
            <div class="absolute md:top-[35%] md:left-[20%] top-[16%] left-[8%] flex flex-col items-center justify-center">
                <h1 class="text-[22px] md:text-[42px] text-white font-bold">Contact</h1>
                <p class="text-[16px] md:text-[22px] text-white text-center w-[343px] md:w-[900px]">The company produces and offers a wide range of automatic traffic enforcement equipment, photo radar systems and intelligent road cameras.</p>
            </div>
            <div class="flex items-center w-[85%] m-auto mt-10">
                <nuxt-link
                    to="/"
                    :class="{ active: isActive('/') }"
                    class="underline"
                >
                    Home
                </nuxt-link>
                <img src="~/assets/product/211607_right_arrow_icon.svg" class="w-[25px] h-[15px]">
                <nuxt-link
                    to="/contact"
                    :class="{ active: isActive('/contact') }"
                >
                   Contact
                </nuxt-link>
            </div>
            <div class="w-[85%] m-auto md:flex justify-between mt-5">
                <img src="~/assets/contact/image 1.png">
                <div class="w-full md:ml-[50px] mt-4 md:mt-0">
                    <form @submit.prevent="handleSubmit">
                        <!-- Name Input -->
                        <div class="mb-8">
                            <input
                            type="text"
                            id="name"
                            v-model="form.name"
                            class="w-full h-[60px] px-3 py-2 bg-blue-100 border border-gray-300 rounded"
                            placeholder="Name"
                            />
                        </div>

                        <!-- Email Input -->
                        <div class="mb-8">
                            <input
                            type="email"
                            id="email"
                            v-model="form.email"
                            class="w-full h-[60px] px-3 py-2 bg-blue-100 border border-gray-300 rounded"
                            placeholder="E-mail"
                            />
                        </div>

                        <!-- Phone Number Input -->
                        <div class="mb-8">
                            <input
                                type="text"
                                id="name"
                                v-model="form.phone_number"
                                class="w-full h-[60px] px-3 py-2 bg-blue-100 border border-gray-300 rounded"
                                placeholder="Phone Number"
                            />
                        </div>

                        <!-- Message Input -->
                        <div class="">
                            <textarea
                                id="message"
                                v-model="form.message"
                                class="w-full px-3 py-2 bg-blue-100 border border-gray-300 rounded"
                                rows="4"
                                placeholder="Message"
                            >
                            </textarea>
                        </div>

                        <!-- Submit Button -->
                    </form>
                </div>
            </div>
            <div class="w-[85%] m-auto">
                <div
                    type="submit"
                    class="w-[210px] h-[63px] ml-auto text-center bg-blue-800 text-white pt-4 rounded hover:bg-blue-600"
                >
                    Send message
                </div>
            </div>
            <div class="mt-[5rem]">
                <img src="~/assets/contact/Map.png" class="w-full">
            </div>
            <div class="w-[85%] m-auto mt-[3rem] md:flex items-start justify-between">
                <div class="border-l-4 border-blue-800 shadow-lg md:w-[480px] flex flex-col justify-center">
                    <h1 class="text-[14px] pl-4 pt-4">Company Address</h1>
                    <h1 class="text-[32px] text-blue-500 pl-4 pb-3 w-[329px]">Themeforest, Envato HQ 24 Fifth st., Los Angeles, USA</h1>
                </div>
                <div class="md:flex mt-5">
                    <div class="w-[285px] flex mt-5 md:mt-0">
                        <img src="~/assets/contact/iconcall.png" class="w-[65px] h-[65px]">
                        <div class="flex flex-col ml-5">
                            <h1 class="mb-1">COMPANY PHONES</h1>
                            <span>+ 1 234 5678 098</span>
                            <span>+ 1 234 5678 098</span>
                        </div>
                    </div>
                    <div class="w-[355px] flex mt-5 md:mt-0">
                        <img src="~/assets/contact/iconemail.png" class="w-[65px] h-[65px]">
                        <div class=" flex flex-col ml-5">
                            <h1 class="mb-1">DUSTRO EMAILS</h1>
                            <span>dustro@gmail.com</span>
                            <span>dustro@gmail.com</span>
                        </div>
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
            form: {
                name: '',
                email: '',
                phone_number: '',
                message: ''
            }
        }
    },
    methods: {
        isActive(route) {
        return this.$route.path === route;
        },
        handleSubmit() {
        // Handle form submission logic
        console.log('Form data:', this.form)
        // You can send the form data to an API or perform other actions here
        }
    }
}
</script>