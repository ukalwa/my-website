<script>
  let isOpen = false;
  function onClickHandler() {
    isOpen = !isOpen;
  }
</script>

<div id="app" class="antialiased text-gray-800 bg-gray-800">
  <header class="container mx-auto sm:flex sm:justify-between">
    <!-- LOGO -->
    <div class="px-4 py-2 flex justify-between items-center font-bold text-2xl">
      <a href="/" aria-label="home" class="text-white">Upender Kalwa</a>
      <div class="sm:hidden">
        <button
          type="button"
          class="block text-gray-500 hover:text-white focus:outline-none"
          on:click="{onClickHandler}"
        >
          <svg class="h-6 w-6 fill-current" viewBox="0 0 24 24">
            {#if !isOpen}
              <path
                fill-rule="evenodd"
                d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0
                2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
              ></path>
            {:else}
              <path
                fill-rule="evenodd"
                d="M18.278 16.864a1 1 0 0 1-1.414 1.414l-4.829-4.828-4.828
                4.828a1 1 0 0 1-1.414-1.414l4.828-4.829-4.828-4.828a1 1 0 0 1
                1.414-1.414l4.829 4.828 4.828-4.828a1 1 0 1 1 1.414 1.414l-4.828
                4.829 4.828 4.828z"
              ></path>
            {/if}
          </svg>
        </button>
      </div>
    </div>
    <div
      class="px-2 py-1 pb-2 text-white {isOpen ? 'block' : 'hidden'} sm:flex"
    >
      <a
        class="block px-2 py-2 rounded font-semibold hover:bg-gray-600"
        href="/publications"
      >
        Publications
      </a>
      <a
        class="block px-2 py-2 rounded font-semibold hover:bg-gray-600"
        href="/blog"
      >
        Blog
      </a>
      <a
        class="block px-2 py-2 rounded font-semibold hover:bg-gray-600"
        href="/contact"
      >
        Contact
      </a>
    </div>
  </header>
</div>

<div class="container mx-auto">
  <slot />
</div>
<footer></footer>
