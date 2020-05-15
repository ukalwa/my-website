<script>
  import About from "../components/About.svelte";
  import Profile from "../components/Profile.svelte";
</script>

<section>
  <div
    class="flex flex-col items-center lg:flex-row px-8 py-2 lg:items-start
    justify-center"
  >
    <Profile />
    <About />
  </div>
</section>
