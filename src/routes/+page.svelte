<script>
    import Navigationbar from "../components/navbar/navbar.svelte";
    import { Heading, Button } from "flowbite-svelte";
    import Footer from "../components/footer/footer.svelte";
    import logo from "$lib/fcs_weiss.png";

    let headingClass = "mb-4 text-white";
</script>

<main>
    <Navigationbar />
    <div class="landing">
        <div class="red-box">
            <img src={logo} alt="FC Sportfreunde Logo" class="logo" />
            <div class="heading">
                <Heading
                    tag="h2"
                    class={headingClass}
                    customSize="text-4xl font-extrabold md:text-4xl lg:text-7xl"
                >
                    Willkommen beim FC Sportfreunde München!
                </Heading>
                <!-- Rotating banner added here -->
                <div class="banner-container">
                    <div class="banner">
                        <span>Jahreshauptversammlung 2025: Kommt vorbei!</span>
                        <span>Liebe Grüße, euer Präsi.</span>
                    </div>
                </div>
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
        position: relative;
    }

    .logo {
        position: absolute;
        top: 13%;
        right: 5%;
        width: 25vw; /* Adjust size relative to viewport width */
        height: auto;
        transform: rotate(30deg); /* Tilt the logo by 30 degrees */
    }

    .heading {
        width: 80%;
        margin-top: 25%;
        margin-left: 20px;
    }

    /* Rotating banner styles */
    .banner-container {
        overflow: hidden;
        width: 100%; /* Adjusted width to fill container */
        height: 40px;
        position: relative;
        background: white;
        border-radius: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 20px;
    }

    .banner {
        display: flex;
        white-space: nowrap;
        animation: slideBanner 8s linear infinite;
        width: 100%; /* Fill the width of the container */
    }

    .banner span {
        padding: 0 30px;
        font-size: 1.2rem;
        font-weight: bold;
        color: black;
    }

    @keyframes slideBanner {
        0% {
            transform: translateX(100%);
        }
        100% {
            transform: translateX(-100%);
        }
    }

    .button-mitglied {
        position: absolute;
        top: 110px;
        right: 20px;
        width: 300px;
        /* height: auto; */
        transform: rotate(25deg);
        transition: transform 0.5sease-in-out;
    }
</style>
