<script lang="ts">
  export let name: string;
  export let title: string;
  export let image: string;
  export let bio: string;
</script>

<div class="bg-white rounded-lg shadow-lg overflow-hidden">
  <img src={image} alt={name} class="w-full h-48 object-cover" />
  <div class="p-6">
    <h3 class="text-xl font-bold mb-2">{name}</h3>
    <p class="text-gray-600 mb-4">{title}</p>
    <p class="text-gray-700">{bio}</p>
  </div>
</div>
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