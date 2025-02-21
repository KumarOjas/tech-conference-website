<script lang="ts">
  const sponsors = [
    {
      name: 'Tech Innovators',
      tier: 'Gold',
      logo: '/images/sponsors/tech-innovators.png',
      url: 'https://techinnovators.com'
    },
    {
      name: 'Cloud Solutions',
      tier: 'Silver', 
      logo: '/images/sponsors/cloud-solutions.png',
      url: 'https://cloudsolutions.com'
    },
    {
      name: 'Data Pioneers',
      tier: 'Bronze',
      logo: '/images/sponsors/data-pioneers.png',
      url: 'https://datapioneers.com'
    }
  ];
</script>


<section class="py-16 px-4">
  <h1 class="text-4xl font-bold text-center mb-12">Sponsors</h1>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
    {#each sponsors as sponsor}
      <div class="p-6 border rounded-lg shadow-sm hover:shadow-md transition-shadow">
        <div class="text-center">
          <img src={sponsor.logo} alt={sponsor.name} class="h-24 mx-auto mb-4" />
          <h3 class="text-xl font-semibold mb-2">{sponsor.name}</h3>
          <span class={`inline-block px-3 py-1 text-sm rounded-full 
            ${sponsor.tier === 'Gold' ? 'bg-yellow-400' : 
              sponsor.tier === 'Silver' ? 'bg-gray-300' : 'bg-amber-700'} 
            text-white`}>
            {sponsor.tier} Sponsor
          </span>
          <a href={sponsor.url} target="_blank" rel="noopener noreferrer" 
             class="mt-4 inline-block text-blue-600 hover:text-blue-800">
            Visit Website
          </a>
        </div>
      </div>
    {/each}
  </div>

</section>
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