<script>    
    import Step from "./Step.svelte";

    let steps = [
        {name: 'Guhas Canvas', icon:'fa-solid fa-palette', link:"https://www.guhascanvas.com/"}, 
        {name: 'Kadhai Surukkam', icon:'fa-solid fa-scroll ', link:"https://kadhai-surukkam.vercel.app/"},
        {name: 'Promptab', icon:'fa-solid fa-terminal', link:"https://promptab.vercel.app/"},
    ];    
</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8
        lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-orange-100">
                Hi! I'm <span class="poppins text-violet-400">Guhaprasaanth</span> Nandagopal <br/>Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes JavaScript (NEXT.JS
                or Sveltekit), Tailwind CSS, Node.js + Express.js & PostgreSQL or Firebase/
                Firestore!
            </p>
            <a href="/" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins
            relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in Touch &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center shadow-2xl">
            <img src={"images/dp.png"} alt="Me" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
            A few of my creative endeavors.
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Curious to <span class="poppins text-violet-400">see</span> my
            work?
        </h3>
        </div>
        <!-- <a
            href="https://www.github.com/guhandelta"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid
            border-white flex items-center gap-2 -mb-4 sm:-mb-0-mt-10
            hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a> -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p class="">Guhas Canvas is an AI Image Generator for </p>
                <strong class="text-violet-400">For artists to create art through prompts</strong>
            </Step>
            <Step step={steps[1]}>
                <p class="">Kadhai Surukkam is an AI Article Summarizer for</p>
                <strong class="text-violet-400">For scholars to summarize huge texts</strong>
            </Step>
            <Step step={steps[2]}>
                <p class="">Promptab is an opensource AI prompting tool for </p>
                <strong class="text-violet-400">For creating and share creative prompts</strong>
            </Step>
        </div>
    </section>
</main>