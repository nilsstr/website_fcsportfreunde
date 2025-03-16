<script>
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import { Card, Heading } from "flowbite-svelte";
    import Footer from "../../components/footer/footer.svelte";
    import herlin from "$lib/herlin.png";
    import avatar from "$lib/avatar.png";
    import avatar_w from "$lib/avatar_w.png";
    import { A } from 'flowbite-svelte';

    // Array of card data
    let VorstandData = [
        {
            image: herlin,
            title: "1. Vorstand & Präsi",
            description: "Herrlin Markja",
            email: "h.markja@fcsportfreunde.de"
        },
        {
            image: avatar,
            title: "2. Vorstand",
            description: "Herbert Schiller",
            email: "h.schiller@fcsportfreunde.de"
        },
        {
            image: avatar,
            title: "Hauptkassier",
            description: "Manuel Langner",
            email: "m.langner@fcsportfreunde.de"
        },
        {
            image: avatar,
            title: "Schriftführer",
            description: "Raffaele Denami",
            email: "r.denami@fcsportfreunde.de"
        },
        {
            image: avatar,
            title: "Technischer Leiter",
            description: "Joseph Wodak",
            email: "j.wodak@fcsportfreunde.de"
        },
        // Add more card objects here if needed
        // Add more card objects here if needed
    ];

    let teamleitungen = [
        {
            image: avatar_w,
            description: "Christiane Heger",
            email: "c.heger@fcsportfreunde.de"
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
                            style="width: auto; height: auto;"
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
                            <A class="font-medium hover:underline">{card.email}</A>
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
                                <A class="font-medium hover:underline">{card.email}</A>
                            </Card>
                        </div>
                    {/each}
                </div>
            </div>
        </div>
    </div>
</main>
<Footer />

<style>
    .home {
        display: flex;
        justify-content: center;
        margin-top: 20px; /* Add margin to create space from the Navigationbar */
        margin-left: 10px;
        margin-right: 10px;
    }

    .card-container {
        margin-top: 100px;
        width: auto;
    }
    .card-margin {
        margin-top: 20px;
    }
</style>
