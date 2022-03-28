<script>
  import Counter from "./Counter.svelte";
  import Input from "./Input.svelte";

  const commonProps = { maxCounter: 9 };
</script>

<section>
  <h1>Search Movies 🍿</h1>
  <Input />
</section>

<!-- <Counter initialCounter={5} {... commonProps}/>
<Counter initialCounter={22} {... commonProps}/>
<Counter {... commonProps}/> -->
<style>
  h1 {
    font-size: 32px;
  }

  section {
    align-items: center;
    display: flex;
    flex-direction: column;
  }
</style>
