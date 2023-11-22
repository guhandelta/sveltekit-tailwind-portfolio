<script>    
    import Step from "./Step.svelte";
    import Exp from "./Exp.svelte";

    let steps = [
        {name:'Guhas Canvas', icon:'fa-solid fa-palette', link:"https://www.guhascanvas.com/"}, 
        {name:'Kadhai Surukkam', icon:'fa-solid fa-scroll ', link:"https://kadhai-surukkam.vercel.app/"},
        {name:'Promptab', icon:'fa-solid fa-terminal', link:"https://promptab.vercel.app/"},
        {name:'GitHub', icon:'fa-brands fa-github', link:"https://github.com/guhandelta"},
    ];    
    
    let experiences = [
        {client:'FreeWire Technologies', location: 'Newark, CA', role: 'Sr Software Developer', period: 'Nov 2022 – Till Date', description: 'Developing UI for the Asset Management Platform, using ReactJS, Material-UI and Redux Toolkit.'}, 
        {client:'Wells Fargo', location: 'Charlotte, NC', role: 'ReactJS Developer', period: 'Jan 2022 - Nov 2022', description: 'Worked with migrating a UI for a brokerage application from JSTL/HTML5 to React JS.'},
        {client:'AT&T', location: 'Plano, TX', role: 'Fullstack Developer', period: 'Feb 2021 - Dec 2021', description: 'Worked on developing a Dashboard application for server utilization analytics using React JS/TypeScript.'},
        {client:'Disciver Financial Services', location: 'Riverwoods, IL', role: 'Fullstack Developer', period: 'Jan 2020 - Jan 2021', description: 'Worked on developing a Dashboard application for server utilization analytics using React JS/TypeScript.'},
        {client:'Barclay Card US', location: 'Parsippany, NJ', role: 'Fullstack Developer', period: 'Sept 2019 - Dec 2020', description: 'Worked developing UI for the credit card portal with some latest features from React 16.8.'},
        {client:'Express Scripts', location: 'Franklin Lakes, NJ', role: 'Fullstack Developer', period: 'Sept 2019 - Dec 2020', description: 'Developed interactive UI to visualize patient data for different diseases along with some insights using ReactJS.'},
        {client:'Blue Shield of California', location: 'San Francisco, CA', role: 'Fullstack Developer', period: 'Sept 2019 - Dec 2020', description: 'Worked on developing UI for Find a Doctor application, using Angular 4/TypeScript and Karma.'},
        {client:'Florida Blue', location: 'Tampa, FL', role: 'Fullstack Developer', period: 'Sept 2019 - Dec 2020', description: 'Worked on developing responsive pages for some sections of the web apps using latest features from Angular 4'},
        {client:'LinkedIn', location: 'Parsippany, NJ', role: 'Fullstack Developer', period: 'Sept 2019 - Dec 2020', description: 'Checkout my LinkedIn Profile'},
        
    ];

    let benefits = [
        {name:'A self taught developer', description: 'I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, backend programming, design, cloud services and much much more.'}, 
        {name:'A UI/UX Enthusiast', description: 'Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.'},
        {name:'Creative collaborator', description: 'Communication is key and it\'s a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.'},
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
            <a href="mailto:guhan.delta@gmail.com" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins
            relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer" target="_blank">
                <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
                <h4 class="relative z-9">Get in Touch &rarr;</h4>
            </a>
        </div>
        <div class="relative grid place-items-center shadow-2xl">
            <img src={"images/dp.png"} alt="Me" class="object-cover z-[2] max-h-[70vh]" />
        </div>
    </section>

    <section id="experience" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Work <span class="poppins text-violet-400">Experience</span>
            </h3>
            <div class="flex flex-col gap-2 text-center">
                <h6 class="text-lg sm:text-xl md:text-2xl">
                    My <span class="text-orange-400 font-bold">Professional</span> Endeavors.
                </h6>
            </div>
        </div>
        <div class="grid grid-cols-2 sm:grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            {#each experiences as proj, index}
                {#if index<8}
                    <Exp exp={experiences[index]}>
                        <p class="text-orange-400">{proj.location}</p>
                        <span class="flex flex-row sm:flex-col sm:mx-auto">
                            <p class="text-violet-400">{proj.role}</p> &emsp;<span class="sm:none"></span>&emsp; <p class="text-teal-400">{proj.period}</p>
                        </span>
                        <strong class="">{proj.description}</strong>
                    </Exp>
                {/if}
            {/each}
            </div>
            <Exp exp={experiences[8]}>
                <p class="text-orange-400 font-bold">{experiences[8].description}</p>
                <!-- <span class="flex flex-row sm:flex-col sm:mx-auto">
                    <p class="text-violet-400">{proj.role}</p> &emsp;<span class="sm:none"></span>&emsp; <p class="text-teal-400">{proj.period}</p>
                </span>
                <strong class="">{proj.description}</strong> -->
            </Exp>
    </section>
    <hr class="">
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Curious to <span class="poppins text-violet-400">see</span> my
            work?
        </h3>
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
        <Step step={steps[3]}>
            <p class="">GitHub</p>
            <strong class="text-violet-400">Explore my current works</strong>
        </Step>
    </section>
    <section id="about" class="relative flex flex-col pt-10 py-20 lg:pt-16 lg:py-32 gap-16 sm:gap-24 md:gap-24">

    <div
        class="flex flex-col gap-2 text-center relative before:absolute before:top-0
        before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute
        after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A bit <span class="poppins text-violet-400">about</span> me.
        </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w- [800px]">
        {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">0{index+1}</p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-2xl md:text-5xl">{benefit.name}</h3>
                    <p class="">{benefit.description}</p>
                </div>
            </div>
        {/each}
    </div>
    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">The <span class="text-violet-400">Complete</span>
        Package</h5>
        <div class="flex flex-col overflow-x-scroll gap-10 max-w- [800px] mx-auto w-full">
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class="border-b border-solid border-slate-200">
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8">Me</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Dedication</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Critical Thoughts</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Team Worker</td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Programming Ability</td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>    
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">So why invest?</p>
    </section>
</main>