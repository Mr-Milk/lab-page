<script>
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
</script>

<style global>
    @import url('https://fonts.googleapis.com/css2?family=Raleway&display=swap');

    body {
        color: #777777;
        background: #f7f7f7;
        font-family: 'Raleway', -apple-system, BlinkMacSystemFont, Roboto, Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
    }
</style>

<Router {routes} />