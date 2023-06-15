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
</script>

<main>
    <Navigationbar />

    <div class="form">
        <div class="header">
            <Heading tag="h2" customSize="text-4xl font-extrabold "
                >Mitgliedschaft</Heading
            >
        </div>
        <form>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
                <div>
                    <Label for="first_name" class="mb-2">Vorname</Label>
                    <Input
                        type="text"
                        id="first_name"
                        placeholder="Vorname"
                        required
                    />
                </div>
                <div>
                    <Label for="last_name" class="mb-2">Nachname</Label>
                    <Input
                        type="text"
                        id="last_name"
                        placeholder="Nachname"
                        required
                    />
                </div>
                <div>
                    <Label for="company" class="mb-2">Geburtstag</Label>
                    <Input
                        type="text"
                        id="company"
                        placeholder="Tag/Monat/Jahr"
                        required
                    />
                </div>
                <div>
                    <Label for="phone" class="mb-2">Geburtsort</Label>
                    <Input
                        type="tel"
                        id="phone"
                        placeholder="Geburtsort"
                        pattern="[0-9]{3}-[0-9]{2}-[0-9]{3}"
                        required
                    />
                </div>
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2">Straße</Label>
                <Input type="email" id="email" placeholder="Straße" required />
            </div>
            <div class="grid gap-6 mb-6 md:grid-cols-2">
                <div>
                    <Label for="first_name" class="mb-2">Wohnort</Label>
                    <Input
                        type="text"
                        id="first_name"
                        placeholder="Wohnort"
                        required
                    />
                </div>
                <div>
                    <Label for="last_name" class="mb-2">Telefon</Label>
                    <Input
                        type="text"
                        id="last_name"
                        placeholder="Telefon"
                        required
                    />
                </div>
                <div>
                    <Label for="first_name" class="mb-2">E-Mail</Label>
                    <Input
                        type="text"
                        id="first_name"
                        placeholder="E-Mail"
                        required
                    />
                </div>
                <div>
                    <Label for="last_name" class="mb-2">Handy</Label>
                    <Input
                        type="text"
                        id="last_name"
                        placeholder="Handy"
                        required
                    />
                </div>
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2">Staatsangehörigkeit</Label>
                <Input
                    type="email"
                    id="email"
                    placeholder="Staatsangehörigkeit"
                    required
                />
            </div>
            <div class="mb-6">
                <Label for="email" class="mb-2"
                    >Letzter Verein/Zuletzt gespielt am/Abgemeldet am</Label
                >
                <Input
                    type="email"
                    id="email"
                    placeholder="(Optional)"
                    required
                />
            </div>
            <div class="bedinungen">
                <P color="text-gray-500 dark:text-gray-400"
                    >Durch meine Bestätigung erkenne ich die Satzung des Vereins an und verpflichte mich zur pünktlichen Zahlung der
                    jährlichen Mitgliedsbeiträge. Die Entrichtung des Beitrages erfolgt durch Bankeinzug (SEPA-Lastschrift) im Januar
                    eines jeden Jahres. Der Austritt ist unter Einhaltung einer Frist von 4 Wochen zum 31.12. zulässig und muss schriftlich
                    an die Postadresse des Vereins angezeigt werden. Einer Bildveröffentlichung des Mitgliedes auf der Internetseite des
                    <A
                        href="/"
                        class="text-primary-700 dark:text-primary-700 hover:underline"
                        >FC Sportfreunde Münchens
                    </A>, in Vereinszeitungen und im Vereinsheim wird zugestimmt.</P
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
            <Button type="Bestätigen">Absenden</Button>
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
