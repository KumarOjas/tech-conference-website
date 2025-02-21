<script>
  import '$lib/app.css';
</script>


<nav class="bg-gray-800 p-4">
  <div class="container mx-auto flex justify-between items-center">
    <a href="/" class="text-white text-xl font-bold">Tech Conference</a>
    <div class="flex space-x-4">
      <a href="/about" class="text-gray-300 hover:text-white">About</a>
      <a href="/schedule" class="text-gray-300 hover:text-white">Schedule</a>
      <a href="/speakers" class="text-gray-300 hover:text-white">Speakers</a>
      <a href="/sponsors" class="text-gray-300 hover:text-white">Sponsors</a>
      <a href="/contact" class="text-gray-300 hover:text-white">Contact</a>
    </div>
  </div>
</nav>

<slot />
<footer class="bg-gray-800 text-white py-8 mt-8">
  <div class="container mx-auto px-4 text-center">
    <p class="text-sm">
      &copy; 2025 Tech Conference. All rights reserved.
    </p>
    <p class="text-xs mt-2">
      Built with <a href="https://kit.svelte.dev" class="text-blue-400 hover:text-blue-600">SvelteKit</a>
    </p>
  </div>
</footer>