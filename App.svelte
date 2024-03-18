<script>
  import Crossword from "../src/Crossword.svelte";
  import dataNYTMini from "./data/nyt-mini.json";
  import dataNYTDaily from "./data/nyt-daily.json";
  import dataOreo from "./data/oreo.json";
  import dataUSA from "./data/usa.json";
  import dataTest from "./data/christopher_thats_hot.txt.json";

  let revealedUSA;
  let theme;
</script>


<article>
  <section id="default" class ="show-large">

    <Crossword data="{dataTest}" />
  </section>

  <section id="default" class = "show-small">

    <Crossword data="{dataTest}" showKeyboard="{true}"/>
  </section>

 
</article>

<style>

/* `contents` prevents wrapper from affecting layout */
  .show-small { display: none; }
  .show-large { display: inline; }

  @media (max-width: 768px) {
    .show-small { display: inline; }
    .show-large { display: none; }
  }
  article {
    max-width: 960px;
    margin: 0 auto;
    padding: 1em;
    font-family: sans-serif;
  }
  .intro {
    text-align: left;
    max-width: 760px;
    font-size: 1.5em;
  }
  section {
    max-width: 960px;
    
  }

  .info {
    max-width: 640px;
    margin: 1em 0;
    text-align: left;
    font-size: 1.125em;
  }
  .info a {
    margin-right: 0.25em;
  }
  h1 {
    font-size: 1.5em;
  }
  h2 {
    font-size: 1.5em;
    padding-top: 1em;
  }
  p {
    margin: 1em auto;
  }

  #themes {
    padding: 1em;
  }

  #themes.dark {
    background: #1a1a1a;
    color: #fff;
  }
  code {
    font-size: 0.85em;
    background-color: #efefef;
    padding: 0 0.25em;
  }

  button {
    cursor: pointer;
  }
</style>
