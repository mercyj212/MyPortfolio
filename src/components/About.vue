<template>
        <section id="about" ref="aboutSection" class="min-h-screen flex flex-col items-center justify-center px-4 md:px-8 pt-24 bg-white text-black" >
            <div 
                data-aos="zoom-in" 
                data-aos-duration="1000" 
                class="w-full max-w-7xl min-h-[460px] md:min-h-[560px] rounded-3xl  bg-white text-black "
            >
                <h1 class="text-5xl md:text-6xl font-bold mt-8 md:mt-16 mb-8 ">About Me</h1>

        

                <div class="grid grid-cols-1 md:grid-cols-2 gap-6 w-full mb-12 px-4 ">   
                    <div class="flex flex-col justify-center text-center md:text-left"
                        data-aos="fade-right"
                        data-aos-duration="800"
                        data-aos-delay="200"
                    >
                        <h2 class="text-3xl md:text-4xl font-semibold mb-4">Hi, I'm Mercy</h2>
                        <p class="text-base md:text-lg text-gray-700 leading-relaxed">
                        A passionate frontend developer dedicated to creating innovative and impactful solutions. With a background in computer science, I specialize in building user-friendly website. My work blends creativity, technical expertise, and a commitment to delivering high-quality results that resonate with audiences.
                        I thrive on tackling challenges and transforming ideas into reality, whether through coding responsive applications. My approach is collaborative, detail-oriented, and always focused on exceeding expectations. When I'm not coding, you can find me exploring new technologies.
                        Let's connect to bring your next project to life!</p>
                    </div>

                    <div class="flex justify-end items-center "  
                        data-aos="fade-left" 
                        data-aos-duration="800" 
                        data-aos-delay="200"
                    >   
                        <img src="../assets/bw.jpg" alt="profile picture" class="w-full max-w-[300px] md:max-w-[400px] h-auto opacity-90 ">
                    </div> 

        
                </div>
            </div>
        </section>
</template>

<script>
    export default {
        mounted() {
          this.$nextTick(() => {
           window.AOS.refresh();
       });
      }
    };
</script> 