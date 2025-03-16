<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
    import avatar_w from "$lib/avatar_w.png";
    import pdfFile from "$lib/JHV2025.pdf";
</script>

<main>
    <Navigationbar />
    <div class="content">
        <div class="header"></div>
            <Heading tag="h2" customSize="text-4xl font-extrabold">Jahreshauptversammlung 2025</Heading>

            <P class="my-4 text-gray-500">
                FC Sportfreunde München e.V. <br />
                am Montag, 17. März 2025 Beginn 19:00 Uhr <br/>
                Vereinsheim Säbener Str.59, 81547 München
            </P>
            <Heading tag="h2" customSize="text-4xl font-extrabold">Tagesordnung</Heading>

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
            <a href={pdfFile} download class="download-link">Download PDF</a>
    </div>
    <Footer />
</main>

<style>
    main {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    .content {
        flex: 1;
        margin: 0 5%;
    }

    .header {
        margin-top: 100px;
    }

    .download-link {
        display: inline-block;
        margin-top: 20px;
        padding: 10px 20px;
        background-color: #1d4ed8;
        color: white;
        text-decoration: none;
        border-radius: 5px;
    }

    .download-link:hover {
        background-color: #2563eb;
    }
</style>
