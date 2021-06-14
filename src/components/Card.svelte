<script>
  export let title;
  export let text;
  export let link;
</script>

<a class="card-body" href={link}>
  <h2>{title}</h2>
  <p>{text}</p>
</a>

<style>
  .card-body {
    width: 50%;
    display: block;
    margin-left: auto;
    margin-right: auto;
    border: 0.01rem solid black;
    border-radius: 1rem;
    padding: 1rem;
    margin-top: 0.6rem;
    margin-bottom: 0.6rem;
  }
</style>
