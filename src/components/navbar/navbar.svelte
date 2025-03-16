<script>
  import {
    Navbar,
    NavBrand,
    NavLi,
    NavUl,
    NavHamburger,
    MegaMenu,
    Chevron
  } from "flowbite-svelte";
  import logo from "$lib/fcs.png";
  import { page } from "$app/stores";
  import { base } from '$app/paths';

  let menu2 = [
    {
      name: "Herren",
      help: "Trainer: Michal Timko",
      href: "herren",
    },
    {
      name: "Herren II",
      help: "Trainer: Niklas Bellino",
      href: "herren2",
    },
  ];
</script>

<svelte:head>
  <link
    rel="stylesheet"
    href="https://unpkg.com/mono-icons@1.0.5/iconfont/icons.css"
  />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
</svelte:head>

<div class="relative px-8">
  <Navbar
    navClass="px-2 sm:px-2 py-2.5 fixed w-full z-20 top-0 left-0 border-b"
    let:hidden
    let:toggle
  >
    <NavBrand href="{base}/">
      <img src={logo} class="mr-3 h-6 sm:h-" alt="fcs Logo" />
      <span
        class="self-center whitespace-nowrap text-l font-semibold dark:text-white"
        >FC Sportfreunde München e.V.</span
      >
    </NavBrand>
    <NavHamburger on:click={toggle} />
    <NavUl {hidden}>
      <NavLi href="{base}/" active={$page.url.pathname === "/"}>Startseite</NavLi>
      <NavLi href="{base}/verein" active={$page.url.pathname === base+"/verein"}
        >Verein</NavLi
      >
	<!--
      <NavLi href="{base}/aktuelles" active={$page.url.pathname === "/aktuelles"}
        >Aktuelles</NavLi
      >
	-->
      <NavLi href="{base}/spiele" active={$page.url.pathname === "/spiele"}
        >Spiele</NavLi
      >

      <NavLi class="cursor-pointer"><Chevron aligned>Herren</Chevron></NavLi>
      <MegaMenu full items={menu2} let:item>
        <a
          href="{base}/{item.href}"
          class="block p-3 rounded-lg hover:bg-gray-50 dark:hover:bg-gray-700 h-full"
        >
          <div class="font-semibold dark:text-white">{item.name}</div>
          <span class="text-sm font-light text-gray-500 dark:text-gray-400"
            >{item.help}</span
          >
        </a>
      </MegaMenu>
      <NavLi href="{base}/Jahreshauptversammlung 2025" active={$page.url.pathname === "/Jahreshauptversammlung 2025"}
        >Jahreshauptversammlung 2025</NavLi
      >
      <NavLi href="{base}/impressum" active={$page.url.pathname === "/impressum"}
        >Impressum</NavLi
      >
      <NavLi href="mailto: info@fcsportfreunde.de">
        <div class="mail">
        <i class="mi mi-email" />
      </div>
      </NavLi>
      <NavLi>
        <div class="insta"> 
          <a href="https://www.instagram.com/fcsportfreunde/" class="fa fa-instagram"></a>
        </div>
      </NavLi>
    </NavUl>
  </Navbar>
</div>

<style>
  .mail {
    height: auto;
    width: auto;
  }
  .mi {
		font-size: x-large;
	}
  .insta {
    height: auto;
    width: auto;
    font-size: x-large;
  }
</style>
