<template>
  <div>
    <h1>jstop.heroku.com</h1>
    <nuxt-link to="/js">js page</nuxt-link>
  </div>
</template>

<script>
    import hljs from 'highlight.js/lib/highlight';
    import javascript from 'highlight.js/lib/languages/javascript';
    import 'highlight.js/styles/ocean.css';

    hljs.registerLanguage('javascript', javascript);
    export default {
        name: "Index",
        mounted() {
            [...document.getElementsByClassName('javascript')].forEach(code => {
                hljs.highlightBlock(code)
            });
            console.log('index page')
        }
    }
</script>