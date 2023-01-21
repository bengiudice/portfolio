<svelte:head>
    <title>Contact</title>
</svelte:head>

<script context="module">
    export const load = async ({ fetch }) => {
        const res = await fetch("https://jsonplaceholder.typicode.com/posts");
        const blogposts = await res.json();
        return {
            props: {
                blogposts,
            }
        }
    }
</script>
<script>
    export let blogposts;
</script>

<div class="container">
    <h1>My projects</h1>
    <div class="projects">
        {#each projects as proj}
        <div class="proj"></div>
        <h2>{proj.title.substring(0, 20)}</h2>
    </div>
</div>