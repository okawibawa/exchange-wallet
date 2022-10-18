<script>
  import "@fontsource/mulish"
  import "@fontsource/mulish/600.css"  
  import "@fontsource/mulish/700.css"  
</script>

<slot></slot>

<style>
  :global(*::before, *::after) {
    box-sizing: border-box;
  }

  :global(*) {
    margin: 0;
  }

  :global(html) {
    width: 100%;
    height: 100%;
  }

  :global(body) {
    position: relative;
    font-family: "Mulish", sans-serif;
    margin: auto;
    height: 100%;
    width: 100%;
    max-width: 600px;
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
  }  
</style>