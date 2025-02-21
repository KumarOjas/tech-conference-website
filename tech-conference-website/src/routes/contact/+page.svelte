<script lang="ts">
  import pkg from 'sveltestrap';
  const { Form, FormGroup, Label, Input, Button } = pkg;

  import { faTwitter, faLinkedin, faFacebook } from '@fortawesome/free-brands-svg-icons';
  import { FontAwesomeIcon } from '@fortawesome/svelte-fontawesome';
</script>

<section class="py-16 px-4">
  <h1 class="text-4xl font-bold text-center mb-12">Contact Us</h1>
  <div class="max-w-3xl mx-auto">
    <Form>
      <FormGroup>
        <Label for="name">Name</Label>
        <Input type="text" bsSize="lg" />
      </FormGroup>
      <FormGroup>
        <Label for="email">Email</Label>
        <Input type="email" bsSize="lg" />
      </FormGroup>
      <FormGroup>
        <Label for="message">Message</Label>
        <Input type="textarea" bsSize="lg" />
      </FormGroup>
      <Button color="primary" block>Send Message</Button>
    </Form>

    <div class="mt-12 text-center">
      <h3 class="text-2xl font-bold mb-4">Follow Us</h3>
      <div class="flex justify-center space-x-6">
        <a href="https://twitter.com" target="_blank" rel="noopener noreferrer" 
           class="text-blue-400 hover:text-blue-600 transition-colors">
          <FontAwesomeIcon icon={faTwitter} size="2x" />
        </a>
        <a href="https://linkedin.com" target="_blank" rel="noopener noreferrer" 
           class="text-blue-700 hover:text-blue-900 transition-colors">
          <FontAwesomeIcon icon={faLinkedin} size="2x" />
        </a>
        <a href="https://facebook.com" target="_blank" rel="noopener noreferrer" 
           class="text-blue-600 hover:text-blue-800 transition-colors">
          <FontAwesomeIcon icon={faFacebook} size="2x" />
        </a>
      </div>
    </div>
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
