<script>
  //  export let current;
    let bmenuOpen = false;

    var openMenu = () => {
        bmenuOpen = !bmenuOpen;
    };

    var closeMenu = () => {
        bmenuOpen = !bmenuOpen;
    };

    //  class:w-2&sol;3={bmenuOpen}
</script>
<style>

nav.visible-m
{
    width: 66.6%;
    opacity: 1;
    visibility: visible;
}






</style>
<div class="sm:p-8 p-2 bg-grey-100">
    <div class="p-1 flex place-content-between md:grid md:grid-cols-3">
        <a href="#"
            ><img class="w-40 h-12" src="assests/logo2.svg" alt="Logo" /></a
        >
        <img
            on:click={openMenu}
            class="md:hidden w-6 h-6 cursor-pointer"
            src="assests/menu.svg"
            alt="Open Navigation"
        />


        <nav   class="md:flex md:static md:justify-end md:bg-transparent md:z-0 md:flex-row-reverse w-0 md:w-full opacity-0 md:opacity-100 h-screen md:h-auto z-50 p-2 transition-all ease-in fixed top-0 right-0 bg-gray-100"
                class:visible-m={bmenuOpen} >
            <img
                on:click={closeMenu}
                class="md:hidden m-2 cursor-pointer float-right"
                src="assests/close-icon.svg"
                alt="Close Navigation"
            />
            <ul class="list-none md:flex m-3">
                <!-- Shift+Alt+[down-arrow-key] for replicating line-->
                <li class="font-bold">
                    <a on:click={closeMenu} href="#main">Home</a>
                </li>
                <!-- <li><a on:click={closeMenu} href="#work">My Work</a></li>
                <li><a on:click={closeMenu} href="#contact">Contact</a></li> -->
            </ul>
        </nav>
    </div>
</div>
