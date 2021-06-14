<script>
  import successkid from "images/successkid.jpg";
  import Card from "../components/Card.svelte";
</script>

<svelte:head>
  <title>Universell Utforming: Internett for alle!</title>
</svelte:head>

<h1>Universell utforming som utvikler</h1>

<Card title="Hva? &rarr" text="Hva er universell utforming?" link="Hva" />
<Card
  title="Hvorfor? &rarr"
  text="Hvorfor skal jeg som utvikler lære noe om dette?"
  link="Hvorfor"
/>
<Card
  title="Hvordan? &rarr"
  text="Hvordan kan jeg utvikle universelt utformede løsninger?"
  link="Hvordan"
/>

<style>
  h1,
  p {
    text-align: center;
    margin: 0 auto;
  }

  h1 {
    font-size: 2.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 0 0 0.5em 0;
  }

  p {
    margin: 1em auto;
  }

  @media (min-width: 480px) {
    h1 {
      font-size: 4em;
    }
  }
</style>
