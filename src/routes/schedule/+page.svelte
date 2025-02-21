<script lang="ts">
  import { Table } from 'sveltestrap';



  const sessions = [
    {
      date: '2025-02-24',
      time: '09:00 - 10:00',
      topic: 'Opening Keynote: The Future of Technology',
      speaker: 'Alex Taylor',
      location: 'Main Hall',
      description: 'Join us for an inspiring opening keynote exploring the latest trends and innovations shaping the future of technology.'
    },
    {
      date: '2025-02-24',
      time: '10:15 - 11:00',
      topic: 'Cloud-Native Architectures',
      speaker: 'Casey Morgan',
      location: 'Room A',
      description: 'Learn how to design and implement cloud-native architectures for modern applications.'
    },
    {
      date: '2025-02-24',
      time: '11:15 - 12:00',
      topic: 'AI in Business Applications',
      speaker: 'Jordan Lee',
      location: 'Room B',
      description: 'Discover practical applications of AI in various business domains and how to implement them effectively.'
    },
    {
      date: '2025-02-25',
      time: '09:00 - 10:00',
      topic: 'Data Science in Practice',
      speaker: 'Taylor Quinn',
      location: 'Main Hall',
      description: 'Real-world case studies and best practices in data science implementation.'
    },
    {
      date: '2025-02-25',
      time: '10:15 - 11:00',
      topic: 'Enterprise Cloud Strategies',
      speaker: 'Morgan Blake',
      location: 'Room A',
      description: 'Strategies for successful cloud adoption and migration in enterprise environments.'
    },
    {
      date: '2025-02-25',
      time: '11:15 - 12:00',
      topic: 'Cybersecurity Best Practices',
      speaker: 'Riley Jordan',
      location: 'Room B',
      description: 'Essential cybersecurity practices to protect your organization in the digital age.'
    }
  ];

</script>


<section class="py-16 px-4">
  <h1 class="text-4xl font-bold text-center mb-12">Schedule</h1>
  <div class="max-w-6xl mx-auto">
    <Table>
      <thead>
        <tr>
          <th>Date</th>
          <th>Time</th>
          <th>Topic</th>
          <th>Speaker</th>
          <th>Location</th>
        </tr>

      </thead>
      <tbody>
        {#each sessions as session}
        <tr>
          <td>{session.date}</td>
          <td>{session.time}</td>
          <td>
            <div class="font-bold">{session.topic}</div>
            <div class="text-sm text-gray-600">{session.description}</div>
          </td>
          <td>{session.speaker}</td>
          <td>{session.location}</td>
        </tr>

        {/each}
      </tbody>

    </Table>
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