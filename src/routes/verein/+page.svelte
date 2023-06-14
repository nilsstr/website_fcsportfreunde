<script>
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import { Card, Heading } from "flowbite-svelte";
    import Footer from "../../components/footer/footer.svelte";
    import andi from "$lib/andi.png";
    import herlin from "$lib/herlin.png";
    // Array of card data
    let VorstandData = [
        {
            image: herlin,
            title: "1. Vorstand",
            description: "Herrlin Markja",
        },
        // Add more card objects here if needed
    ];

    let MitgliederData = [
        {
            image: andi,
            title: "Platzwart",
            description: "Max Mustermann",
        },
        // Add more card objects here if needed
    ];
</script>

<main>
    <Navigationbar />
    <div class="home">
        <div class="card-container">
            <div class="heading-title">
                <Heading tag="h3" customSize="text-3xl font-extrabold "
                    >Vereinsführung</Heading
                >
            </div>
            {#each VorstandData as card}
                <div class="card-margin">
                    <Card
                        {card}
                        horizontal
                        img={card.image}
                        style="width: 600px; height: 200px;"
                    >
                        <!-- svelte-ignore a11y-img-redundant-alt -->
                        <h5
                            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                        >
                            {card.description}
                        </h5>
                        <p
                            class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"
                        >
                            {card.title}
                        </p>
                    </Card>
                </div>
            {/each}
        </div>
        <div class="card-container">
            <div class="heading-title">
                <Heading tag="h3" customSize="text-3xl font-extrabold "
                    >Weitere Ämter</Heading
                >
            </div>
            {#each MitgliederData as card}
                <div class="card-margin">
                    <Card
                        {card}
                        horizontal
                        img={card.image}
                        style="width: 600px; height: 200px;"
                    >
                        <!-- svelte-ignore a11y-img-redundant-alt -->
                        <h5
                            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                        >
                            {card.description}
                        </h5>
                        <p
                            class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight"
                        >
                            {card.title}
                        </p>
                    </Card>
                </div>
            {/each}
        </div>
    </div>
    <Footer />
</main>

<style>
    .home {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .card-container {
        margin-top: 100px;
    }
    .card-margin {
        margin-top: 20px;
        margin-bottom: 20px;
    }
</style>
