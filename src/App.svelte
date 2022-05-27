<script>
    import Settings from "./Settings.svelte";
    import Dashboard from "./Dashboard.svelte";
    import Profile from "./Profile.svelte";
</script>

<main>
    <div class="container">
        <div class="page">
            <Settings />
            <Dashboard />
            <Profile />
        </div>
    </div>
</main>

<style>
    .page {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(100%, 1fr));
        grid-template-areas: "dashboard";
    }
    @media (min-width: 1280px) {
        .page {
            display: grid;
            grid-template-columns: minmax(284px, 1fr) 3fr minmax(375px, 1fr);
            grid-template-areas: "setting dashboard profile";
        }
    }
</style>
