<script>
    import { Route } from 'tinro';
    import About from './pages/About.svelte';
    import Home from './pages/Home.svelte';
    import Contacts from './pages/Contacts.svelte';
    // import SubContent from './pages/SubContent.svelte';
</script>

<Route path="/" redirect="/home"><Home /></Route>
<Route path="/home"><Home /></Route>
<Route path="/about/*">
    <!-- 반드시 *을 사용해야함 (router.svelte에서 띄우든, 상위 page에 component로 포함시키든) -->
    <About />
    <!-- <Route path="/sub">
        <SubContent />
    </Route> -->
</Route>
<Route path="/contacts"><Contacts /></Route>
