<script lang="ts">
    export let name: string;

    const vendors = [
        {
            name: "Stuller Fine Jewelry",
            logoImg: "image13",
            description: "Stuller, Inc. is the #1 supplier of fine jewelry, findings, mountings, tools, packaging, diamonds & gemstones for today's retail jeweler."
        },
        {
            name: "Quality Gold",
            logoImg: "image14",
            description: "Actively serving more than 23,000 retailers across the United States, its territories and within Canada, Quality Gold offers more than 200,000 jewelry & gift products available to ship same day and more than 100,000 items available special order for sale to retailers."
        },
        {
            name: "Rembrandt Charms",
            logoImg: "image15",
            description: "Rembrandt Charms. The world's largest charm collection available in sterling silver, 10 karat gold, 14 karat white or yellow gold and gold plate."
        },
        {
            name: "Overnight Mountings",
            logoImg: "image16",
            description: "With over 50000 mountings and semi-mounts, Overnight Mountings has one of the largest in-stock inventories in the industry."
        },
    ]
</script>

<main>
    <h1 id="business-name">{name}</h1>
    <p>
        We love our customers, so feel free to visit during normal business hours!
    </p>
    <section>
        <h2 id="contact">Contact</h2>
        <div>
            <span>Phone: </span><a href="tel:360-385-5012">(360) 385-5012</a>
        </div>
        <br/>
        <div>
            <p>Address:</p>
            <address id="address">
                Lisa's Jewelry<br/>
                99 Oak Bay Rd, Port Hadlock<br/>
                Washington 98339<br/>
                United States<br/>
            </address>
        </div>
    </section>

    <section>
        <h2 id="hours">Hours</h2>
        <ul>
            <li>Mon <em>11:00 am – 03:00 pm</em></li>
            <li>Tue <em>11:00 am – 03:00 pm</em></li>
            <li>Wed <em>11:00 am – 03:00 pm</em></li>
            <li>Thu <em>11:00 am – 03:00 pm</em></li>
            <li>Fri <em>11:00 am – 03:00 pm</em></li>
            <li>Sat <em>By Appointment</em></li>
            <li>Sun <em>Closed</em></li>
        </ul>
    </section>

    <section>
        <h2 id="About">About</h2>
        <p>
            Forty-one years ago, Lisa Petrick was sleeping in an onion field in an old Volkswagen bus. She was 17 and
            working swing shift for Raytheon in Santa Clara, California, where she straightened semiconductor “legs” on
            an assembly line. She had struck out on her own right after her 16th birthday with nothing but a few
            blankets and a few changes of clothes. When winter came, a Yugoslav immigrant and auto mechanic, who Lisa
            remembers only as Zarko, allowed her to park the bus inside his shop where she’d be warmer, and safe.
        </p>
        <p>
            In Zarko’s shop, she met his friend, 54-year-old Heinar Tamme, a hand engraver of such things as signet
            rings (for the pope, the Kennedys, Sammy Davis Jr., among others). “He actually invited me up to see his
            etchings,” she recalls, laughing.
        </p>
        <p>
            Heinar, who had escaped the Nazis by skiing from Estonia across the Baltic Sea to Finland, recognized a kid
            who needed help. He gave her a place to live, bought her clothes, paid her to work as his apprentice and
            taught her his trade.
        </p>
        <p>
            He also introduced her to his wife, Laura, who taught her bookkeeping, and to goldsmith Robin Barnes, who
            had been trained in Europe. Between the three of them, they launched Lisa into goldsmithing, a career she
            has practiced for the past 30 years at Lisa’s Jewelry.
        </p>
        <p>
            “I wanted to call my shop ‘The Little Girl in the Back,’ because that’s how people identified me for the
            first 19 years I worked with Heinar on Water Street,” she says.
        </p>
        <p>
            A few years ago, after Laura had died, Heinar had a debilitating stroke. Lisa brought him to her home to
            recuperate for nine months. When he had been stabilized and was yearning to go home, she paid for his return
            to Estonia, for his room in a care center and round-the-clock nursing care. He passed away there in 2009.
        </p>
    </section>

    <section>
        <h2 id="services">Services</h2>
        <ul>
            <li>jewelry repair</li>
            <li>pearl &amp; bead restringing</li>
            <li>14 karat gold</li>
            <li>sterling silver</li>
            <li>gems</li>
            <li>same day sizing</li>
            <li>watch repair</li>
            <li>watch batteries</li>
            <li>curbside service</li>
        </ul>
    </section>

    <section>
        <h2>Vendors</h2>

        <ul>
            {#each vendors as v}
                <li>
                    <div>{v.name}</div>
                    <img src="{v.logoImg}" alt="img" />
                    <div>{v.description}</div>
                </li>
            {/each}
        </ul>
    </section>
</main>

<style>
    main {
        /*text-align: center;*/
        padding: 1em;
        /*max-width: 240px;*/
        margin: 0 auto;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

    h2 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 2em;
        font-weight: 100;
    }

    ul {
        text-align: left;
    }

    @media (min-width: 640px) {
        main {
            /*padding: 0;*/
            max-width: 640px;
        }
    }
</style>