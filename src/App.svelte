<script>
   import { Router, Link, Route } from "svelte-routing";
   import Home from "./routes/Home.svelte";
  import Blog from "./routes/Blog.svelte";
  export let url = "";
</script>

<Router url="{url}">
  <div class="flex flex-col">
  <nav class="bg-gray-200 px-10 py-5 flex gap-10">
    <Link to="/">Home</Link>
    <Link to="blog">Blog</Link>
  </nav>
  <div class="px-24">
    <Route path="blog" component="{Blog}" />
    <Route path="/"><Home /></Route>
  </div>
</div>
</Router>