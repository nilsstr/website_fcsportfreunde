<script>
  import { Heading, P } from "flowbite-svelte";
  import Navigationbar from "../../components/navbar/navbar.svelte";
  import Footer from "../../components/footer/footer.svelte";
  import { onMount } from 'svelte';
  import config from './config.json'; 


  let widgetOptions = {
    height: '500',
    width: '1100',
    selectedTab: 'spiele',
    colorResults: 'rgb(0,0,0)',
    colorNav: 'rgb(0,0,0)',
    colorClubName: 'rgb(0,0,0)',
    backgroundNav: 'undefined',
  };

  onMount(() => {
    const script = document.createElement('script');
    script.type = 'text/javascript';
    script.src = 'https://widget-prod.bfv.de/widget/widgetresource/widgetjs';

    script.onload = () => {
      window.BFVWidget.HTML5.zeigeVereinSpiele(
        config.id,
        config.bfv_id,
        widgetOptions
      );
    };

    document.head.appendChild(script);
  });
</script>

<main>
  <Navigationbar />
  <div class="header">
    <Heading tag="h2" customSize="text-4xl font-extrabold "
      >Tabellenübersicht</Heading
    >
    <div id={config.bfv_id} class="spiel-tabelle">Laden...</div>
  </div>
  
</main>
<Footer />

<style>
  main {
    display: flex;
    flex-direction: column;
  }

  .navbar {
    order: 1;
  }

  .footer {
    order: 3;
  }

  .header {
    order: 2;
    margin-top: 100px;
    width: 80%; /* Adjust the width value as needed */
    margin-left: auto;
    margin-right: auto;
    justify-content: center;
    display: grid;
  }
  .spiel-tabelle{
    margin-top: 20px;
  }
</style>
