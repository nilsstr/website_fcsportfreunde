<script>
    import { Heading} from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
    import Beitrag_1 from "../blog/1_beitrag/+page.md";
    import Beitrag_2 from "../blog/2_beitrag/+page.md";
</script>

<main>
    <Navigationbar />
    <div class = 'header'>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Aktuelles vom FC Sportfreunde</Heading
        >
        <Beitrag_2></Beitrag_2>
        <Beitrag_1></Beitrag_1>
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