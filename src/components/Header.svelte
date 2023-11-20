
<script>
    export let y;

    let tabs=[
        { name: "About", link: "#about" },
        { name: "Projects", link: "#projects" },
        { name: "Contact", link: "#contact" }
    ];
</script>

<header class={"sticky z-[10] top-0 duration-200 flex items-center justify-between border border-solid" + (
    y>0 
        ? "py-4 bg-slate-950 border-violet-950"
        : "py-6 bg-transparent border-transparent"
)}>
    <h1 class="font-medium">
        <b class="font-bold poppins">Guhaprasaanth</b> Nandagopal
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab}
            <a href={tab.link} class="duration-200 hover: text-violet-400">
                <p class="">{tab.name}</p>
            </a>
        {/each}
    </div>
        <a 
            href="mailto:guhan.delta@gmail.com"
            target="_blank"
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white
            text-slate-950"
        >
            <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
            group-hover:translate-x-full z-0 duration-200" />
            <h4 class="relative z-9">Get in Touch</h4>
        </a>

</header>
