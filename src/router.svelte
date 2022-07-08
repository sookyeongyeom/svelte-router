<script>
    import { Route } from 'tinro';
    import About from './components/About.svelte';
    import Home from './components/Home.svelte';
    import Contacts from './components/Contacts.svelte';
    // import SubContent from './pages/SubContent.svelte';
    import Transition from './Transition.svelte';
</script>

<Transition>
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
    <Route fallback>No page found</Route>
</Transition>
