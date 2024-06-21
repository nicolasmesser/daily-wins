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
      <h1 class="text-3xl font-bold"><a href="/">Daily Wins</a></h1>
      <p>You need 3 daily wins:</p>
      <ul class="list-disc list-inside">
        <li>a physical win (walking, running, swimming, ...)</li>
        <li>a mental win (reading, writing, creating, learning, ...)</li>
        <li>a spiritual win (meditating, studying, growing, ...)</li>
      </ul>
      <p class="font-bold">Be a complete winner!</p>
    </div>
  </main>
</AppLayout>
