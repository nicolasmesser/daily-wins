<script>
  import { ThemeSelect } from 'svelte-ux';
  import { AppBar } from 'svelte-ux';
  import { AppLayout } from 'svelte-ux';
</script>

<AppLayout areas="'header header' 'aside main'">
  <svelte:fragment slot="nav">
    <!-- Nav menu -->

  </svelte:fragment>

  <AppBar title="Daily Wins">

    <div slot="actions">
      <!-- App actions -->
      <ThemeSelect />
    </div>
  </AppBar>

  <main>
    <slot />
    <div class="container px-8">
      <h1 class="text-3xl font-bold">Daily Wins</h1>
      <p>You need 3 daily wins:</p>
      <ul class="list-disc list-inside">
        <li>a <a href="/physical">physical</a> win (walking, running, swimming, ...)</li>
        <li>a <a href="/mental">mental</a> win (reading, writing, creating, learning, ...)</li>
        <li>a <a href="/spiritual">spiritual</a> win (meditating, studying, growing, ...)</li>
      </ul>
      <p class="font-bold">Be a complete winner!</p>
    </div>
  </main>
</AppLayout>
