<script>
    import "../app.css";
    import Header from '../components/Header.svelte';
    import Footer from '../components/Footer.svelte';

    let y;
    let innerHeight;
    let innerWidth;

    function goTop(){
        document.body.scrollIntoView();
    }
</script>

<div class="relative flex flex-col max-w-[1440px] mx-auto w-full text-sm sm:text-base min-h-screen top-4">
    <div class={"fixed bottom-0 w-full duration-200 flex px-10 z-[10]"+
        (y > 0 
            ? "opacity-100 pointer-events-auto" 
            : "opacity-0 pointer-events-none")
    }>
        <button on:click={goTop} class="ml-auto rounded-full aspect-square bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
            <i class="fa-solid fa-arrow-up grid place-items-center aspect-square" />
        </button>
    </div>
    <Header />
    <slot />
    <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />