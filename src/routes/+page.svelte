<script>
    import Navigationbar from "../components/navbar/navbar.svelte";
    import { Heading, Button } from "flowbite-svelte";
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
                <div class= "button-mitglied">
                    <Button color="light" href="/mitgliedschaft">
                        Jetzt Mitglied werden<svg
                            aria-hidden="true"
                            class="ml-2 -mr-1 w-5 h-5"
                            fill="currentColor"
                            viewBox="0 0 20 20"
                            xmlns="http://www.w3.org/2000/svg"
                            ><path
                                fill-rule="evenodd"
                                d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z"
                                clip-rule="evenodd"
                            /></svg
                        >
                    </Button>
                </div>
            </div>

            <div class="container-ball">
                <img src={Soccerball} class="ball" alt="ball" />
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
    .container-ball {
        align-items: right;
        width: 100%;
    }
    .button-mitglied {
        margin-top: 40px;
    }
</style>
