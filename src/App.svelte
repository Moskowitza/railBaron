<script>
  export let name;

  import Destination from "./Destinations.svelte";
  import Header from "./Header.svelte";
  import HomeCity from "./HomeCity.svelte";
  import Footer from "./Footer.svelte";
</script>

<style>
  .wrapper {
    min-height: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr auto 50px;
  }
</style>

<div class="wrapper">
  <Header />
  <HomeCity/>
  <Destination />
  <Footer />
</div>
