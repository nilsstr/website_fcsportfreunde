<script>
  import { Heading, P } from "flowbite-svelte";
  import Navigationbar from "../../components/navbar/navbar.svelte";
  import Footer from "../../components/footer/footer.svelte";
  import { onMount } from "svelte";
  import config from "./config.json";

  let widgetOptions = {
    height: "500",
    width: "1100",
    selectedTab: "spiele",
    colorResults: "rgb(0,0,0)",
    colorNav: "rgb(0,0,0)",
    colorClubName: "rgb(0,0,0)",
    backgroundNav: "undefined",
  };

  onMount(() => {
    const script = document.createElement("script");
    script.type = "text/javascript";
    script.src = "https://widget-prod.bfv.de/widget/widgetresource/widgetjs";

    script.onload = () => {
      window.BFVWidget.HTML5.zeigeVereinSpiele(
        config.id_herren,
        config.bfv_id_herren,
        widgetOptions
      );
    };

    document.head.appendChild(script);
  });
</script>

<!-- 
 - Trainingszeiten
 - Trainerinfo Nummer etc. 
 -->

<body>
  <Navigationbar />
  <div class="header">
    <Heading tag="h2" customSize="text-4xl font-extrabold">Jugend</Heading>
    <Footer />
  </div>
</body>

<style>
  .navbar {
    order: 1;
  }

  .footer {
    order: 3;
  }

  .header {
    order: 2;
    margin-top: 100px;

    text-align: center;
    display: list-item;
  }
  .spiel-tabelle {
    margin-top: 2%;
    width: 100%;
    display: flex;
    justify-content: center;
  }
</style>
