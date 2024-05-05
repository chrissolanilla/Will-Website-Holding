<script>
    import Navbar from "$lib/components/Nav.svelte"
    import About from "$lib/components/About.svelte"
    import Approach from "$lib/components/Approach.svelte"
    import CoreValues from "$lib/components/CoreValues.svelte"
    import TargetMarkets from "$lib/components/TargetMarkets.svelte"
    import Team from "$lib/components/Team.svelte"
    import Contact from "$lib/components/Contact.svelte"
</script>

<Navbar />

<h1>Welcome to Bill Website</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<div id="About"><About /></div>
<div id="Approach"><Approach /></div>
<div id="Values"><CoreValues /></div>
<div id="Target"><TargetMarkets /></div>
<div id="Team"><Team /></div>
<div id="Contact"><Contact /></div>

