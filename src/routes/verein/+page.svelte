<script>
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import { Card, Heading } from "flowbite-svelte";
    import Footer from "../../components/footer/footer.svelte";
    import herlin from "$lib/herlin.png";
    import avatar from "$lib/avatar.png";
    // Array of card data
    let VorstandData = [
        {
            image: herlin,
            title: "1. Vorstand",
            description: "Herrlin Markja",
        },
        {
            image: avatar,
            title: "2. Vorstand",
            description: "Herbert Schiller",
        },
        {
            image: avatar,
            title: "Hauptkassier",
            description: "Manuel Langner",
        },
        {
            image: avatar,
            title: "Schriftführer",
            description: "Raffaele Denami",
        }
        // Add more card objects here if needed
        // Add more card objects here if needed
    ];

    let teamleitungen = [
        {
            image: avatar,
            description: "Christiane Heger",
        },
        {
            image: avatar,
            description: "Amir Seferovic",
        }
    ];
</script>

<main>
    <Navigationbar />
    <div class="home">
        <div class="card-container">
            <div class="heading-title">
                <Heading tag="h3" customSize="text-3xl font-extrabold "
                    >Vorstandschaft</Heading
                >
            </div>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
            {#each VorstandData as card}
                <div class="card-margin">
                    <Card
                        {card}
                        horizontal
                        img={card.image}
                        style="width: 500px; height: 200px;"
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
                    >Jugendleitung</Heading
                >
            </div>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
            {#each teamleitungen as card}
                <div class="card-margin">
                    <Card
                        {card}
                        horizontal
                        img={card.image}
                        style="width: 500px; height: 200px;"
                    >
                        <!-- svelte-ignore a11y-img-redundant-alt -->
                        <h5
                            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
                        >
                            {card.description}
                        </h5>
                    </Card>
                </div>
            {/each}
        </div>
        </div>
</main>
<Footer />

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
