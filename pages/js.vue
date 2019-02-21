<template>
  <div>
    <h1>Js page</h1>
    <nuxt-link to="/">
      Главная
    </nuxt-link>
    <pre>
      <code class="javascript">
    console.log('highlight js code')
  </code>
  </pre>
    <span>test highlight</span>
    <pre>
      <code class="javascript">
    let arr = ['banan', 'apple', 'lemon'];
        arr.forEach(fruit => {
          console.log(fruit)
        })
  </code>
  </pre>
  </div>
</template>

<script>
    import hljs from 'highlight.js/lib/highlight';
    import javascript from 'highlight.js/lib/languages/javascript';
    import 'highlight.js/styles/ocean.css';

    hljs.registerLanguage('javascript', javascript);

    export default {
        name: "Js",
        mounted() {
            [...document.getElementsByClassName('javascript')].forEach(code => {
                hljs.highlightBlock(code)
            });
            console.log('index page')
        }
    }
</script>