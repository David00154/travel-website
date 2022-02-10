<svelte:head>
    <!-- font awesome cdn link  -->
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</svelte:head>

<script>
import "../../static/css/style.css"
import Header from "$lib/header.svelte"
import Footer from "$lib/footer.svelte"
</script>

<Header />
<slot />
<Footer />
