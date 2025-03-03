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
    }

    .heading {
        width: 80%;
        margin-top: 25%;
        margin-left: 50px;
    }

    /* Rotating banner styles */
    .banner-container {
        overflow: hidden;
        width: 100%;
        max-width: 500px;
        height: 40px;
        position: relative;
        background: rgba(0, 0, 0, 0.5);
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
    }

    .banner span {
        padding: 0 30px;
        font-size: 1.2rem;
        font-weight: bold;
        color: white;
    }

    @keyframes slideBanner {
        0% { transform: translateX(100%); }
        100% { transform: translateX(-100%); }
    }

    .button-mitglied {
        margin-top: 40px;
    }
</style>
