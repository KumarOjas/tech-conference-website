<script lang="ts">
  import { onMount } from 'svelte';
  export let targetDate: Date;

  let timeLeft = {
    days: 0,
    hours: 0,
    minutes: 0,
    seconds: 0
  };

    let interval: ReturnType<typeof setInterval>;


  const calculateTimeLeft = () => {
    const difference = +targetDate - +new Date();
    if (difference > 0) {
      timeLeft = {
        days: Math.floor(difference / (1000 * 60 * 60 * 24)),
        hours: Math.floor((difference / (1000 * 60 * 60)) % 24),
        minutes: Math.floor((difference / 1000 / 60) % 60),
        seconds: Math.floor((difference / 1000) % 60)
      };
    }
  };

  onMount(() => {
    calculateTimeLeft();
    interval = setInterval(calculateTimeLeft, 1000);
    return () => clearInterval(interval);
  });
</script>

<div class="flex justify-center space-x-4 text-white">
  <div class="text-center">
    <div class="text-4xl font-bold">{timeLeft.days}</div>
    <div class="text-sm">Days</div>
  </div>
  <div class="text-center">
    <div class="text-4xl font-bold">{timeLeft.hours}</div>
    <div class="text-sm">Hours</div>
  </div>
  <div class="text-center">
    <div class="text-4xl font-bold">{timeLeft.minutes}</div>
    <div class="text-sm">Minutes</div>
  </div>
  <div class="text-center">
    <div class="text-4xl font-bold">{timeLeft.seconds}</div>
    <div class="text-sm">Seconds</div>
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