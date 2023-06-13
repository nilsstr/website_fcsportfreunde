<script>
    import { Heading, P } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";
</script>

<main>
    <Navigationbar />
    <div class="header">
        <Heading tag="h2" customSize="text-4xl font-extrabold ">Adresse</Heading
        >

        <P class="my-4 text-gray-500">
            FC Sportfreunde München <br />
            Säbener Straße 59 <br />
            81547 München
        </P>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Haftung für Inhalte</Heading
        >

        <P class="my-4 text-gray-500">
            Die Inhalte unserer Seiten wurden mit größter Sorgfalt erstellt. Für
            die Richtigkeit, Vollständigkeit und Aktualität der Inhalte können
            wir jedoch keine Gewähr übernehmen. <br /> <br />
            Als Diensteanbieter sind wir gemäß § 6 Abs.1 MDStV und § 8 Abs.1 TDG
            für eigene Inhalte auf diesen Seiten nach den allgemeinen Gesetzen verantwortlich.
            Diensteanbieter sind jedoch nicht verpflichtet, die von ihnen übermittelten
            oder gespeicherten fremden Informationen zu überwachen oder nach Umständen
            zu forschen, die auf eine rechtswidrige Tätigkeit hinweisen. Verpflichtungen
            zur Entfernung oder Sperrung der Nutzung von Informationen nach den allgemeinen
            Gesetzen bleiben hiervon unberührt. Eine diesbezügliche Haftung ist jedoch
            erst ab dem Zeitpunkt der Kenntnis einer konkreten Rechtsverletzung möglich.
            Bei bekannt werden von entsprechenden Rechtsverletzungen werden wir diese
            Inhalte umgehend entfernen.
        </P>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Haftung für Links</Heading
        >

        <P class="my-4 text-gray-500">
            Unser Angebot enthält Links zu externen Webseiten Dritter, auf deren
            Inhalte wir keinen Einfluss haben. Deshalb können wir für diese
            fremden Inhalte auch keine Gewähr übernehmen. Für die Inhalte der
            verlinkten Seiten ist stets der jeweilige Anbieter oder Betreiber
            der Seiten verantwortlich. Die verlinkten Seiten wurden zum
            Zeitpunkt der Verlinkung auf mögliche Rechtsverstöße überprüft.
            Rechtswidrige Inhalte waren zum Zeitpunkt der Verlinkung nicht
            erkennbar. Eine permanente inhaltliche Kontrolle der verlinkten
            Seiten ist jedoch ohne konkrete Anhaltspunkte einer Rechtsverletzung
            nicht zumutbar. Bei bekannt werden von Rechtsverletzungen werden wir
            derartige Links umgehend entfernen.
        </P>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Urheberrecht</Heading
        >

        <P class="my-4 text-gray-500">
            Die Betreiber der Seiten sind bemüht, stets die Urheberrechte
            anderer zu beachten bzw. auf selbst erstellte sowie lizenzfreie
            Werke zurückzugreifen.
            <br /><br />
            Die durch den FC Sportfreunde erstellten Inhalte und Werke auf diesen
            Seiten unterliegen dem deutschen Urheberrecht. Beiträge Dritter sind
            als solche gekennzeichnet. Die Vervielfältigung, Bearbeitung, Verbreitung
            und jede Art der Verwertung außerhalb der Grenzen des Urheberrechtes
            bedürfen der schriftlichen Zustimmung des jeweiligen Autors bzw. Erstellers.
            Downloads und Kopien dieser Seite sind nur für den privaten, nicht kommerziellen
            Gebrauch gestattet.
        </P>
        <Heading tag="h2" customSize="text-4xl font-extrabold "
            >Datenschutz</Heading
        >

        <P class="my-4 text-gray-500">
            Soweit auf unseren Seiten personenbezogene Daten (beispielsweise
            Name, Anschrift oder eMail-Adressen) erhoben werden, erfolgt dies
            soweit möglich stets auf freiwilliger Basis. Die Nutzung der
            Angebote und Dienste ist, soweit möglich, stets ohne Angabe
            personenbezogener Daten möglich. <br /> <br />
            Der Nutzung von im Rahmen der Impressumspflicht veröffentlichten Kontaktdaten
            durch Dritte zur Übersendung von nicht ausdrücklich angeforderter Werbung
            und Informationsmaterialien wird hiermit ausdrücklich widersprochen.
            Die Betreiber der Seiten behalten sich ausdrücklich rechtliche Schritte
            im Falle der unverlangten Zusendung von Werbeinformationen, etwa durch
            Spam-Mails, vor.
        </P>
    </div>
</main>
<div>
    <Footer />
</div>

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
        width: 50%; /* Adjust the width value as needed */
        margin-left: auto;
        margin-right: auto;
    }
</style>
