<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
</script>

<main>
    <Navigationbar />
    <div class = 'header'>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Aktuelles vom F.C. S.</Heading
        >

        <P class="my-4 text-gray-500">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Amet
            cursus sit amet dictum sit. Quis enim lobortis scelerisque fermentum
            dui faucibus in. Mattis vulputate enim nulla aliquet porttitor lacus
            luctus accumsan. Ipsum dolor sit amet consectetur adipiscing elit.
            Euismod nisi porta lorem mollis aliquam ut porttitor. Tortor
            consequat id porta nibh. Tortor condimentum lacinia quis vel eros
            donec ac odio. Elementum sagittis vitae et leo duis ut diam quam
            nulla. Vel turpis nunc eget lorem.
        </P>
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