<script context="module">
  import {Client} from '../../prismic-config'
    export async function load({page}) {
      document = await Client.getSingle('about')
      const { params } = page
        return { props: { params: params, document: document } } 
    }
</script>

<script>
  export let document
</script>


  <pre>{document}</pre>

