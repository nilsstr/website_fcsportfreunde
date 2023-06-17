<!-- post.svelte -->
<script>
    export let title;
    export let date;
</script>

    <div class = "blog">
        <h6
            class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white header"
        >
            {title}
        </h6>
        <p class="font-normal text-gray-700 dark:text-gray-400 leading-tight date">
            Veröffentlicht: {date}
        </p>
        <p>
            <slot />
        </p>
    </div>

<style>
    .blog {
        margin-top: 50px;
        width: 100%; /* Adjust the width value as needed */
        margin-right: auto;
        margin-left: auto;
        box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 3px 0px, rgba(0, 0, 0, 0.06) 0px 1px 2px 0px;
        border-radius: 25px;
        padding: 25px; /* Add space with padding */
    }

    .header {
  font-weight: 600;
  color: black;
  background-clip: text;
  -webkit-background-clip: text;
    }
    .date {
        margin-bottom: 20px;
    }
    .blog-image {
        margin-left: 10px; /* Adjust the margin as needed */
    }
</style>
