<template>
    <section id="contact" class="min-h-screen  bg-black text-white ">
        <div class="flex justify-center items-start px-8 py-12 space-x-12">
            <div   class="w-1/3 space-y-8 mt-30">
                <h2  data-aos="zoom-in" data-aos-duration="800" class="text-3xl font-bold">CONTACT INFO</h2>
                <div class="space-y-4">
                    <div data-aos="fade-right" data-aos-duration="800" class="flex items-center space-x-4">
                        <div  data-aos-duration="800" class="bg-white/10 px-4 py-2 rounded-md shadow"><ion-icon name="mail-outline"></ion-icon></div>
                        <div>
                            <p class="text-white/25">Mail me</p>
                            <p>mercy@gmail.com</p>
                        </div>
                    </div>
                   
                    <div  data-aos="fade-right" data-aos-duration="700"class="flex items-center space-x-4">
                        <div class="bg-white/10 px-4 py-2 rounded-md shadow"><ion-icon name="call-outline"></ion-icon></div>
                        <div>
                            <p class="text-white/25">Call me</p>
                            <p>+234-802-532-7839</p>
                            
                        </div>
                    </div>
                    
                    <div data-aos="fade-right" data-aos-duration="600" class="flex items-center space-x-4">
                        <div class="bg-white/10 px-4 py-2 rounded-md shadow"><ion-icon name="location-outline"></ion-icon></div>
                        <div>
                            <p class="text-white/25">Location</p>
                            <p>Lagos, Nigeria.</p>
                            
                        </div>
                    </div>

                    <div data-aos="fade-right" data-aos-duration="500" class="flex items-center space-x-4">
                        <div class="text-lg font-bold"><p>SOCIAL INFO</p>
                            <div  class="flex space-x-4">
                              <div data-aos="fade-left" data-aos-duration="800" class="bg-white/9 px-4 py-2 rounded-full mb-1"><ion-icon name="at-outline"></ion-icon></div> 
                              <div data-aos="fade-left" data-aos-duration="600" class="bg-white/9 px-4 py-2 rounded-full mb-1"><ion-icon name="logo-twitter"></ion-icon></div>
                              <div data-aos="fade-left" data-aos-duration="400" class="bg-white/9 px-4 py-2 rounded-full mb-1"><ion-icon name="logo-instagram"></ion-icon></div>
                            </div>
                        </div>
                       
                    </div>

                </div>
            </div>

            <div data-aos="fade-left" data-aos-duration="800" class="w-2/4 relative rounded-lg px-4 py-2 shadow-lg backdrop-blur-md bg-white/8  flex flex-col items-center min-h-[300px] md:min-h-[360px] mt-15">
                <h1 class="text-4xl font-bold mb-15">Lets Work Together</h1>

                <form action="" class="space-y-6">
                    <input type="text" placeholder="Name *" class="w-full bg-white/4 p-3 rounded-md">
                    <input type="email" placeholder="Email *" class="w-full bg-white/4 p-3 rounded-md">
                    <input type="text" placeholder="Your Subject *" class="w-full bg-white/4 p-3 rounded-md">
                    <textarea placeholder="Your Message *" class="w-full bg-white/4 p-3 rounded-md h-32"></textarea>
                </form>

                <button type="submit" class=" bg-transparent p-3 rounded-md hover:bg-white/5">Send Message</button>

            </div>
        </div>

     
    </section>
</template>

<script>
    export default {
        mounted() {
            this.$nextTick(() => {
                windows.AOS.refresh();
            })
        }
    }
</script>