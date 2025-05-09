<script lang="ts">
    type Formula = {
        name: string;
        desc: string;
        price: number;
        included: string[];
    };

    const formulae: Formula[] = [
        {
            name: "Basic",
            desc: "For the average WECEAF attendee. All talks are available to you, so you won't miss out on what matters most: our engaging speakers.",
            price: 39999,
            included: [
                "Access to all talks and the recordings afterwards",
                "Complementary lunch from Monday to Saturday",
                "Access to the book signing session by prof. Ronié on Sunday",
            ],
        },
        {
            name: "Pro",
            desc: "For those attendees that want that extra touch out of their WECEAF visit. With Pro, you'll really have something to talk about when you get back from Prague. Attention: if you're in academia, you may be egligible for the Academic formula.",
            price: 79999,
            included: ["Everything included in the Basic package", "Daily access to the Trunk Lounge, where speakers and other Pro attendees can socialise in the mornings and evenings", "Exclusive elephant auto-fellatio footage, captured by prof. Versmøldera in the Mozambique steppe"],
        },
        {
            name: "Academic",
            desc: "For attendees that hold a position in academia. You enjoy a significant discount over the Pro package, while retaining all the benefits.",
            price: 54999,
            included: ["Everything included in the Pro package."],
        },
        {
            name: "Suite",
            desc: "Choosing this package means you're VIP. The best of the best. Simple as that.",
            price: 139999,
            included: ["A luxurious suite in the conference hotel, with access to the rooftop pool and bar", "Access to the VIP Trunk Lounge, where only you and a select group of people can meet our speakers in a more informal setting — with champagne aplenty", "Lifetime access to EleCam, a research project which sends you live webcam footage of elephant auto-fellatio", "Access to our private rooms throughout the day"],
        },
    ];
</script>

<h1 class="text-5xl font-bold text-indigo-800">Buy your WECEAF tickets</h1>
<p>
    Like many conferences nowadays, the WECEAF sells its tickets through a
    Registrar Policy account. This ensures that our attendees are certain of a
    safe ticket delivery, validity of the ticket at the point of arrival and
    most importantly a smooth and hassle-free sale experience. This means you
    have to set up an RP account by <a
        href="mailto:weceaf.conferentie@gmail.com"
        class="text-blue-500 underline">talking to one of our assistants</a
    >.
</p>

<h2 class="text-3xl font-bold text-indigo-800">Our formulae</h2>
<div class="w-full flex flex-row gap-4 [&>div]:flex-1">
    {#each formulae as formula}
        <div class="rounded-md p-6 bg-white flex flex-col justify-between">
            <div class="flex flex-col gap-2">
                <p class="text-xl font-bold">{formula.name}</p>
                <p>{formula.desc}</p>
                <p class="my-2 font-bold">What's included?</p>
                <ul class="list-disc list-inside">
                    {#each formula.included as incl}
                        <li>{incl}</li>
                    {/each}
                </ul>
            </div>

            <p class="text-xl text-indigo-500 font-bold mt-6">
                €{formula.price / 100}
            </p>
        </div>
    {/each}
</div>
