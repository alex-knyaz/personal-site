<script>
import ThemeSwitch from '../components/ThemeSwitch.svelte';

</script>

<main>
  <header>
    <div>
      <h1>
        <slot name="title" ></slot>
      </h1>
      <small>
        <slot name="subtitle"></slot>
      </small>
    </div>
    <ThemeSwitch />
  </header>

  <slot></slot>
</main>