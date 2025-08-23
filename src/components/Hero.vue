<template>
    <section id="home" class="min-h-screen bg-white flex items-center justify-center px-4 md:px-8 pt-24 h-20">

        <!-- <div class="absolute -top-20 left-1/2 -translate-x-1/2 w-[600px] bg-purple-500 rounded-full blur-[180px] opacity-40"> -->

        

        <div class="w-full max-w-6xl min-h-[460px] md:min-h-[560px] bg-gradient-to-r from-gray-900 via-black to-gray-900 rounded-3xl overflow-hidden relative flex items-center justify-center ">

          <div class="absolute inset-0 bg-[linear-gradient(to_right,rgba(255,255,255,0.06)-1px,transparent_1px),linear-gradient(to_bottom,rgba(255,255,255,0.06)_1px,transparent_1px)] bg-[size:40px_40px] opacity-30 pointer-events-none">
          </div>

          
            <div  class=" flex flex-col items-center justify-center text-center relative z-10"
            >
                <div class="relative inline-block">
                    <p class="text-9xl font-extrabold text-white tracking-wider" 
                     data-aos="fade-up"
                        :data-aos-delay="index * 100"
                        data-aos-duration="800"
                        data-aos-easing="ease-in-out">MERCY</p>
                      <h1 class="absolute -top-0 left-20 text-sm  tracking-widest  font-bold text-gray-400 leading-tight -mb-6">Hi, I'm      
                      </h1>
                    <p class="absolute left-1/2 -translate-x1/2 font-bold  text-gray-400 -mt-2">a Frontend Developer</p>
                </div>
            </div>
        </div>
       
    </section>
</template>