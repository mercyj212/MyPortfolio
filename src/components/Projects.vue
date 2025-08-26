<template>
    <section id="projects"
        ref="projectSection"
        class="min-h-screen flex flex-col items-center justify-center px-4 md:px-8 pt-24 bg-white"
    >
        <div
            data-aos="fade-up"
            data-aos-duration="1000"
            class="w-full max-w-7xl min-h-[460px] md:min-h-[560px] rounded-3xl shadow-2xl backdrop-blur-md bg-black border border-black text-white pt-16"
        >
            <h1
                class="text-5xl md:text-6xl font-bold mt-8 md:mt-16 mb-8 text-center bg-clip-text text-transparent bg-white"
                data-aos="zoom-in"
                data-aos-duration="800"
            >
                My Projects
            </h1>
            <div v-if="loading" class="text-center">Loading projects...</div>
            <div v-else-if="error" class="text-center text-red-400">
                Failed to load projects. Please try again later.
            </div>
            <div v-else class="flex justify-center">
                <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mb-12">
                    <div
                        v-for="(project, index) in projects.slice(0, 3)"
                        :key="project.id"
                        class="relative rounded-lg p-4 shadow-lg backdrop-blur-md bg-white/10 border border-white/20 flex flex-col items-center min-h-[300px] md:min-h-[360px]"
                        data-aos="fade-up"
                        :data-aos-delay="index * 100"
                        data-aos-duration="800"
                        data-aos-easing="ease-in-out"
                    >
                        <img
                            v-if="project.image"
                            :src="project.image"
                            :alt="`Image for ${project.name}`"
                            class="w-full h-32 md:h-48 object-cover rounded-md mb-2"
                        />
                        <h2 class="text-base font-semibold mb-1 text-center">{{ project.name }}</h2>
                        <p class="text-sm mb-2 text-center flex-1">{{ project.description }}</p>
                        <a
                            v-if="project.link && isValidUrl(project.link)"
                            :href="project.link"
                            target="_blank"
                            rel="noopener noreferrer"
                            class="text-white/45  text-sm hover:text-white transition-colors duration-200 bg-white/20 px-4 py-2 rounded-md"
                            @click="handleLinkClick(project.link)"
                            :aria-label="`View ${project.name} project`"
                        >
                            View
                        </a>
                        <span v-else class="text-gray-400 text-sm">
                            Project link unavailable
                        </span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            loading: true,
            error: null,
            projects: []
        };
    },
    methods: {
        handleLinkClick(link) {
            console.log(`Attempting to navigate to: ${link}`);
        },
        isValidUrl(url) {
            try {
                new URL(url);
                return true;
            } catch {
                return false;
            }
        }
    },
    async mounted() {
        try {
            // Simulate fetching data (replace with real API or actual project URLs)
            this.projects = [
                {
                    id: 1,
                    name: "Portfolio Website",
                    description: "A personal portfolio website built with Vue.js and Tailwind CSS.",
                    image: "https://picsum.photos/400/200?random=1",
                    link: "https://github.com"
                },
                {
                    id: 2,
                    name: "Task Manager",
                    description: "A simple task manager app to organize your daily tasks.",
                    image: "https://picsum.photos/400/200?random=2",
                    link: "https://todoist.com"
                },
                {
                    id: 3,
                    name: "Blog Platform",
                    description: "A modern blog platform for sharing articles and ideas.",
                    image: "https://picsum.photos/400/200?random=3",
                    link: "https://medium.com"
                }
            ];
            this.loading = false;
            this.$nextTick(() => {
                window.AOS.refresh(); // Refresh AOS to detect rendered elements
            });
        } catch (err) {
            this.error = err.message;
            this.loading = false;
        }
    }
};
</script>