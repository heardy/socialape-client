<script>
  import { Router, Link, Route } from 'svelte-routing';
  import Navbar from './components/Navbar.svelte';
  import Home from './routes/Home.svelte';
  import Login from './routes/Login.svelte';
  import Signup from './routes/Signup.svelte';
  import Error from './routes/Error.svelte';

  export let url = "";
</script>

<Router url="{url}">
  <Navbar />
  <div>
    <Route path="/" component={Home} />
    <Route path="login" component={Login} />
    <Route path="signup" component={Signup} />
    <Route patth="*" component={Error} />
  </div>
</Router>
