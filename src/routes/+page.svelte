<script>
    import Navigationbar from "../components/navbar/navbar.svelte";
    import { Heading } from "flowbite-svelte";
    import Footer from "../components/footer/footer.svelte";
    import Soccerball from "$lib/soccer_ball.png";

    let headingClass = "mb-4 text-white";
</script>

<main>
    <Navigationbar />
    <div class="landing">
        <div class="red-box">
            <div class="text-box">
                <Heading
                    tag="h1"
                    class={headingClass}
                    customSize="text-3xl font-extrabold md:text-4xl lg:text-6xl"
                >
                    Willkommen beim FC Sportfreunde München!
                </Heading>
            </div>
            <div class="container-ball">
                <img src={Soccerball} class="ball"  alt="ball"/>
            </div>
        </div>
        <Footer />
    </div>
</main>

<style>
    .red-box {
        background-color: red;
        height: 700px; /* Adjust the height value as needed */
        display: flex;
        align-items: center;
        justify-content: left;
    }

    .white-text {
        color: white;
        font-size: 20px;
    }
    .text-box {
        text-align: left;
        margin-left: 40px;
        width: 70%;
    }
    .ball {
        align-items: right;
        display: flex;
        margin-top: 70px;
    }
    .container-ball{
        align-items: right;
        width: 100%;

    }
</style>
