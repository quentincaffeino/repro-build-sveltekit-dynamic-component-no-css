<script context="module">
  export const prerender = true;

  export async function load() {
    return {
      props: {
        Counter: (await import("$lib/Counter.svelte")).default,
      },
    };
  }
</script>

<script>
  export let Counter;
</script>

<section>
  <svelte:component this={Counter} />
</section>
