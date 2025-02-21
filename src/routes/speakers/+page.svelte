<script lang="ts">
  import SpeakerCard from '$lib/components/SpeakerCard.svelte';
  
  const allSpeakers = [
    {
      name: 'Alex Taylor',
      title: 'Technology Strategist',
      image: '/images/speakers/speaker1.jpg',
      bio: 'Focuses on emerging technologies and their business applications.'
    },
    {
      name: 'Casey Morgan',
      title: 'Software Architect',
      image: '/images/speakers/speaker2.jpg',
      bio: 'Specializes in scalable system design and cloud-native solutions.'
    },
    {
      name: 'Jordan Lee',
      title: 'Innovation Consultant',
      image: '/images/speakers/speaker3.jpg',
      bio: 'Helps organizations adopt cutting-edge technologies effectively.'
    },
    {
      name: 'Taylor Quinn',
      title: 'Data Science Lead',
      image: '/images/speakers/speaker4.jpg',
      bio: 'Expert in machine learning and data-driven decision making.'
    },
    {
      name: 'Morgan Blake',
      title: 'Cloud Solutions Engineer',
      image: '/images/speakers/speaker5.jpg',
      bio: 'Specializes in enterprise cloud migrations and optimizations.'
    },
    {
      name: 'Riley Jordan',
      title: 'Cybersecurity Specialist',
      image: '/images/speakers/speaker6.jpg',
      bio: 'Focuses on enterprise security and threat prevention strategies.'
    }
  ];
</script>


<section class="py-16 px-4">
  <h1 class="text-4xl font-bold text-center mb-12">Speakers</h1>
  <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
    {#each allSpeakers as speaker}
      <SpeakerCard
        name={speaker.name}
        title={speaker.title}
        image={speaker.image}
        bio={speaker.bio}
      />
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