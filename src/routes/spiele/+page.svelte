<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
</script>

<main>
    <Navigationbar />
    <div class = 'header'>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Tabellenübersicht</Heading
        >
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
  }
</style>