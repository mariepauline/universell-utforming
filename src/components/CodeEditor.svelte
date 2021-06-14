<script>
  export let title;

  export let codeText;
</script>

<div class="main-editor">
  <textarea bind:value={codeText} placeholder="Enter HTML to see preview" />
  <iframe {title} class="second" srcdoc={codeText} />
</div>

<style>
  .main-editor {
    height: 20rem;
    width: 100%;
  }
  textarea,
  iframe {
    height: 100%;
    width: 49%;
  }
  textarea {
    text-align: start;
  }
</style>
