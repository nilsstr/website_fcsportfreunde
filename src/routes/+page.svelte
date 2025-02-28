<script>
    import Navigationbar from "../components/navbar/navbar.svelte";
    import { Heading, Button } from "flowbite-svelte";
    import Footer from "../components/footer/footer.svelte";

    let headingClass = "mb-4 text-white";
</script>

<main>
    <Navigationbar />
    <div class="landing">
        <div class="red-box">
            <div class="heading">
                <Heading
                    tag="h1"
                    class={headingClass}
                    customSize="text-4xl font-extrabold md:text-4xl lg:text-7xl"
                >
                    Willkommen beim FC Sportfreunde München!
                </Heading>
            </div>
            <div style="width: 40%" />
        </div>
        <Footer />
    </div>
</main>

<style>
    .red-box {
        height: 700px; /* Adjust the height value as needed */
        width: 100%;
        display: flex;
        background-image: url("$lib/Feld_1.jpg");
        background-size: cover; /* Adjust as needed */
        background-position: center; /* Adjust as needed */
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .heading {
        width: 80%;
        margin-top: 25%;
        margin-left: 50px;
    }

    .button-mitglied {
        margin-top: 40px;
    }
</style>
