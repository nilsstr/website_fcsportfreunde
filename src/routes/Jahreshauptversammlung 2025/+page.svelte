<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
</script>

<main>
    <Navigationbar />
    <div class="header">
        <Heading tag="h2" customSize="text-4xl font-extrabold">
            Jahreshauptversammlung 2025
        </Heading>

        <P class="my-4 text-gray-500">
            FC Sportfreunde München e.V. <br />
            am Montag, 17. März 2025, Beginn 19:00 Uhr <br />
            Vereinsheim Säbener Str. 59, 81547 München
        </P>

        <Heading tag="h2" customSize="text-4xl font-extrabold">
            Tagesordnung
        </Heading>

        <ul class="my-4 text-gray-500 list-decimal list-inside space-y-2">
            <li>Begrüßung und Eröffnung durch den 1. Vorstand</li>
            <li>Feststellung der ordnungsgemäßen Einberufung und der Beschlussfähigkeit der Versammlung</li>
            <li>Bericht des 1. Vorstands</li>
            <li>Bericht des Technischen Leiters</li>
            <li>Bericht der Jugendleitung</li>
            <li>Bericht des Kassiers</li>
            <li>Bericht der Revisoren</li>
            <li>Wahl des Wahlausschusses</li>
            <li>Entlastung der Vorstandschaft</li>
            <li>Neuwahlen</li>
            <li>Verschiedenes</li>
        </ul>
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
        margin-left: 5%;
        margin-right: 5%;
    }
</style>
