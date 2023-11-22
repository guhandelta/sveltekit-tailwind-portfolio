<script>
    export let exp;
</script>
<a
    href="https://www.linkedin.com/in/guhaprasaanthnandagopal/"
    target="_blank"
    class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-violet-700 text-center group cursor-pointer hover:border-violet-400 duration-200"
>
    <div class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200">
        { #if exp.client === "LinkedIn"}  
            <i class="fa-brands fa-linkedin"></i> 
        {:else} 
            <i class="fa-solid fa-briefcase" />
        {/if}
    </div>
    <h1 class="font-medium text-xl sm:text-2xl md:text-1xl">{exp.client}</h1>
    <slot />
    <div class="flex-1 flex justify-between gap-4 items-center">
        <div class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:w-full after:h-full after:bg-white after:duration-200 hover:after:rounded-tr-lg hover:after:rounded-bl-lg hover:after:translate-x-full after:z-[-1] overflow-hidden"
        >   
        { #if exp.client === "LinkedIn"}  
            <p class="relative z-4 p-1 ">Go to &rarr; </p>
        {/if}
        </div>
    </div>
</a>