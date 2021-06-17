<script>
  import CodeEditor from "../components/CodeEditor.svelte";
</script>

<section>
  <h1>Eksempler</h1>
  <p>
    Videre følger noen eksempler på dårlig og god universell utforming. Disse er
    kreativt laget av meg og ikke tatt fra reelle sider i dag, og er bare ment
    for å illustrere hvordan man kan holde utseende likt men legge god
    tilgjengelighet i bunnen.
  </p>


<section>
  <h2>Eksempel på dårlig struktur</h2>
  <div class="example">
    <div class="box code">
      <pre><code>
{`<div class="heading">
  <div class="header-large">
    Hello
  </div>
  <div class="undertitle">
    Welcome to my site
  </div>
</div>
<div class="section">
  <div class="text">
    I hope you enjoy the content.
  </div>
  <div class="text">
    Here is a picture of a dog:
    <img
      src="--link--"
      width="250"
      alt="Dog in water"
    />
  </div>
</div>

<style>
  .header-large {
    font-size: 2em;
    margin: 0 0 0.5em 0;
    font-weight: 400;
    line-height: 1.2;
  }
  .text,
  .undertitle {
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    font-weight: bold;
  }
</style>
`}
    </code></pre>
    </div>
    <div class="box">
      <div class="heading">
        <div class="header-large">Hello</div>
        <div class="undertitle">Welcome to my site</div>
      </div>
      <div class="section">
        <div class="text">I hope you enjoy the content.</div>
        <div class="text">Here is a picture of a dog:</div>
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/These_dogs_love_the_water.JPG/1200px-These_dogs_love_the_water.JPG"
          width="250"
        />
      </div>
    </div>
  </div>
</section>

<h2>Eksempel med bedre struktur og bildetekst</h2>
<div class="example">
  <div class="box code">
    <pre><code>
{`<header>
<h1>Hello</h1>
<p>Welcome to my site</p>
</header>
<section>
<p>I hope you enjoy the content.</p>
<p>
  Here is a picture of a dog:
  <img
    src="--link--"
    width="250"
    alt="Dog in water"
  />
</p>
</section>
    `}
    </code></pre>
  </div>
  <div class="box">
    <header>
      <h1>Hello</h1>
      <p><strong>Welcome to my site</strong></p>
    </header>
    <section>
      <p>I hope you enjoy the content.</p>
      <p>
        Here is a picture of a dog:
        <img
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/These_dogs_love_the_water.JPG/1200px-These_dogs_love_the_water.JPG"
          alt="A happy dog in a boat"
          width="250"
        />
      </p>
    </section>
  </div>
</div>

<p>
  Disse viser at forskjellen i utseende på HTML som bruker semantiske tags 
  og kode som ikke bruker det ikke trenger å gi resultat som ser veldig annerledes ut.
  Det er korte eksempler, men viser likevel at kode med bedre semantikk og derfor
  bedre tilgjengelighet for skjermlesere kan være kortere enn kode som bare bruker 
  klasser.
  Nå bruker det gode eksempelet bare standard-styling for <code>h1</code> og <code>p</code> tags,
  så i alle tilfeller vil nok ikke forskjellen i lengde være så stor så det er en svakhet, 
  men det understreker poenget.
</p>

</section>


<style>
  .example {
    display: flex;
    flex-flow: row wrap;
  }
  .box {
    display: block;
    border: 0.1rem solid black;
    width: 23rem;
    padding: 1rem;
  }
  .header-large {
    font-size: 2em;
    margin: 0 0 0.5em 0;
    font-weight: 400;
    line-height: 1.2;
  }
  .text,
  .undertitle {
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
  }
  .undertitle {
    font-weight: bold;
  }
</style>
