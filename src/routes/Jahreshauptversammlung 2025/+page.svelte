<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
</script>

<main>
    <Navigationbar />
    <div class="header">
        <Heading tag="h2" customSize="text-4xl font-extrabold ">Jahreshauptversammlung 2025</Heading
        >

        <P class="my-4 text-gray-500">
            FC Sportfreunde München e.V. <br />
            am Montag, 17. März 2025 Beginn 19:00 Uhr <br/>
            Vereinsheim Säbener Str.59, 81547 München
        </P>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Tagesordnung</Heading
        >

        <P class="my-4 text-gray-500">
            1. Begrüßung und Eröffnung durch den 1.Vorstand<br/>
            2. Feststellung der ordnungsgemäßen Einberufung und der Beschlussfähigkeit der Versammlung<br/>
            3. Bericht des 1.Vorstands<br/>
            4. Bericht des Technischen Leiters<br/>
            5. Bericht der Jugendleitung<br/>
            6. Bericht des Kassiers<br/>
            7. Bericht der Revisoren<br/>
            8. Wahl des Wahlausschusses<br/>
            9. Entlastung der Vorstandschaft<br/>
            10. Neuwahlen<br/>
            11. Verschiedenes
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
        margin-left: 5%;
        margin-right: 5%;
    }
</style>
