<script>
  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    Chevron,
    MegaMenu,
  } from "flowbite-svelte";
  import logo from "$lib/fcs.png";

  let menu2 = [
    {
      name: "Herren",
      help: "Trainer: Max Mustermann",
    },
    {
      name: "Herren II",
      help: "Trainer: Max Mustermann",
    }
  ];
</script>

<div class="relative px-8">
  <Navbar
    navClass="px-2 sm:px-4 py-2.5 absolute w-full z-20 top-0 left-0 border-b"
    let:hidden
    let:toggle
  >
    <NavBrand href="/">
      <img src={logo} class="mr-3 h-6 sm:h-9" alt="fcs Logo" />
      <span
        class="self-center whitespace-nowrap text-xl font-semibold dark:text-white"
        >F.C. Sportfreunde München</span
      >
    </NavBrand>
    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="/" active={true}>Startseite</NavLi>
      <NavLi href="/aktuelles">Aktuelles</NavLi>
      <NavLi href="/spiele">Spiele</NavLi>
      <NavLi class="cursor-pointer"><Chevron aligned>Teams</Chevron></NavLi>
      <MegaMenu full items={menu2} let:item>
        <a
          href="/"
          class="block p-3 rounded-lg hover:bg-gray-50 dark:hover:bg-gray-700 h-full"
        >
          <div class="font-semibold dark:text-white">{item.name}</div>
          <span class="text-sm font-light text-gray-500 dark:text-gray-400"
            >{item.help}</span
          >
        </a>
      </MegaMenu>
      <NavLi href="/kontakt">Kontakt</NavLi>
    </NavUl>
  </Navbar>
</div>

