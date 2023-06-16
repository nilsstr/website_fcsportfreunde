<script>
    import {
        Label,
        Input,
        Checkbox,
        Button,
        A,
        Heading,
        P,
    } from "flowbite-svelte";
    import Navigationbar from "../../components/navbar/navbar.svelte";
    import Footer from "../../components/footer/footer.svelte";

    import { onMount } from "svelte";

    let name = "";
    let vorname = "";
    let geburtstag = "";
    let geburtsort = "";
    let strasse = "";
    let wohnort = "";
    let telefon = "";
    let email = "";
    let handy = "";
    let staat = "";
    let letzterVerein = "";

    const handleSubmit = async () => {
        const response = await fetch("http://127.0.0.1:8000/your-fastapi-backend-endpoint", {
            method: "POST",
            headers: {
                "Content-Type": "application/json",
            },
            body: JSON.stringify({ name, vorname, geburtstag, geburtsort, strasse, wohnort, telefon, email, handy, staat, letzterVerein }),
        });

        // Handle the response from the backend as per your requirements
        const data = await response.json();
        console.log(data);
    };
</script>

<main>
    <Navigationbar />

    <div class="form">
        <div class="header">
            <Heading tag="h2" customSize="text-4xl font-extrabold "
                >Mitgliedschaft</Heading
            >
        </div>
        <form on:submit|preventDefault={handleSubmit}>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
                <div>
                    <Label for="first_name" class="mb-2">Vorname</Label>
                    <Input
                        type="text"
                        placeholder="Vorname"
                        bind:value={name}
                        required
                    />
                </div>
                <div>
                    <Label for="last_name" class="mb-2">Nachname</Label>
                    <Input
                        type="text"
                        placeholder="Nachname"
                        bind:value={vorname}
                        required
                    />
                </div>
                <div>
                    <Label for="birthday" class="mb-2">Geburtstag</Label>
                    <Input
                        type="text"
                        placeholder="Tag/Monat/Jahr"
                        bind:value={geburtstag}
                        required
                    />
                </div>
                <div>
                    <Label for="birthplace" class="mb-2">Geburtsort</Label>
                    <Input
                        type="text"
                        placeholder="Geburtsort"
                        bind:value={geburtsort}
                        required
                    />
                </div>
            </div>
            <div class="mb-6">
                <Label for="street" class="mb-2">Straße</Label>
                <Input
                    type="text"
                    placeholder="Straße"
                    bind:value={strasse}
                    required
                />
            </div>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
                <div>
                    <Label for="place" class="mb-2">Wohnort</Label>
                    <Input
                        type="text"
                        placeholder="Wohnort"
                        bind:value={wohnort}
                        required
                    />
                </div>
                <div>
                    <Label for="telefone" class="mb-2">Telefon</Label>
                    <Input
                        type="text"
                        placeholder="Telefon"
                        bind:value={telefon}
                        required
                    />
                </div>
                <div>
                    <Label for="email" class="mb-2">E-Mail</Label>
                    <Input
                        type="text"
                        placeholder="E-Mail"
                        bind:value={email}
                        required
                    />
                </div>
                <div>
                    <Label for="handy" class="mb-2">Handy</Label>
                    <Input
                        type="text"
                        placeholder="Handy"
                        bind:value={handy}
                        required
                    />
                </div>
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2">Staatsangehörigkeit</Label>
                <Input
                    type="text"
                    placeholder="Staatsangehörigkeit"
                    bind:value={staat}
                    required
                />
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2"
                    >Letzter Verein/Zuletzt gespielt am/Abgemeldet am</Label
                >
                <Input
                    type="text"
                    placeholder="(Optional)"
                    bind:value={letzterVerein}
                />
            </div>
            <div class="bedinungen">
                <P color="text-gray-500 dark:text-gray-400"
                    >Durch meine Bestätigung erkenne ich die Satzung des Vereins
                    an und verpflichte mich zur pünktlichen Zahlung der
                    jährlichen Mitgliedsbeiträge. Die Entrichtung des Beitrages
                    erfolgt durch Bankeinzug (SEPA-Lastschrift) im Januar eines
                    jeden Jahres. Der Austritt ist unter Einhaltung einer Frist
                    von 4 Wochen zum 31.12. zulässig und muss schriftlich an die
                    Postadresse des Vereins angezeigt werden. Einer
                    Bildveröffentlichung des Mitgliedes auf der Internetseite
                    des
                    <A
                        href="/"
                        class="text-primary-700 dark:text-primary-700 hover:underline"
                        >FC Sportfreunde Münchens
                    </A>, in Vereinszeitungen und im Vereinsheim wird
                    zugestimmt.</P
                >
            </div>
            <div class="checkbox">
                <Checkbox class="mb-6 space-x-1" required
                    >Ich habe die<A
                        href="/"
                        class="text-primary-700 dark:text-primary-700 hover:underline"
                        >Satzung des FC Sportfreunde Münchens
                    </A>&nbsp;gelesen und akzeptiere diese.</Checkbox
                >
            </div>
            <Button type="submit">Absenden</Button>
        </form>
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
        margin-top: 20px;
        width: 80%; /* Adjust the width value as needed */
        margin-left: true;
        margin-right: auto;
        margin-bottom: 30px;
    }

    .form {
        order: 2;
        margin-top: 100px;
        width: 80%; /* Adjust the width value as needed */
        margin-left: auto;
        margin-right: auto;
    }
    .bedingungen {
        margin-top: 20px;
        margin-bottom: 500px;
    }

    .checkbox {
        margin-top: 20px;
        margin-bottom: 20px;
    }
</style>
