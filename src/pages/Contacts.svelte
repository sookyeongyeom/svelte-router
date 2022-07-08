<script>
    import { router } from 'tinro';

    const goHome = () => router.goto('home');
</script>

<h1>Contacts Page</h1>
<p class="on" on:click={goHome}>Go Home!</p>

<!--
router.goto('/foo'); // URL: /foo
router.location.query.set('name', 'alex') // URL: /foo?name=alex
router.location.hash.set('bar') // URL: /foo?name=alex#bar
router.location.query.set('page', '1') // URL: /foo?name=alex#page=1#bar
router.location.query.replace({hello: 'world'}) // URL: /foo?hello=world#bar
router.location.query.clear() // URL: /foo#bar
router.location.hash.clear() // URL: /foo
-->
<style>
    .on {
        cursor: pointer;
    }
</style>
