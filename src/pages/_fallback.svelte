<script>
    import { url } from '@roxi/routify';
    import { Container } from 'svelte-materialify';
</script>

<style>

  .e404 {
    text-align: center;
    padding: 50px;
  }
</style>

<Container>
  <div class="e404">
    <span style="font-size: 40px;">404</span>
    <p>Page not found.
      <!-- link to the parent folder of _fallback.svelte -->
      <a href={$url('/')}>Home</a>
    </p>
  </div>
</Container>

