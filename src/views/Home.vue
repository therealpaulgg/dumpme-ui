<template>
    <div class="home">
        <h1>Dump Me</h1>
        <p>A dumping ground to dump your files</p>
        <DropAndUrls />
    </div>
</template>

<script>
// @ is an alias to /src
import DropAndUrls from "@/components/DropAndUrls.vue"

export default {
    name: "Home",
    components: {
        DropAndUrls,
    },
}
</script>
