<script>
    import { Route } from 'tinro';
    import SubContent from '../components/SubContent.svelte';
</script>

<h1>About Page</h1>
<a href="/about/sub/">Sub</a>

<hr />

<Route path="/sub">
    <SubContent />
</Route>

<hr />
