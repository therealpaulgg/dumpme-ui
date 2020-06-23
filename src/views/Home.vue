<template>
    <v-container class="home">
        <p>A dumping ground to dump your files</p>
        <h4>How it works</h4>
        <p>
            You upload your files to the server. It encrypts the filenames and
            the contents of them using AES-GCM written in Go.
        </p>
        <p>
            After encryption is finished, you are given a download link, which
            stores the name of the directory of your files, as well as the key.
            When you go to this download link, the server will decrypt the files
            using this key, and zip them up and return them to you.
        </p>
        <p>
            <b
                >Note: This is not end-to-end encryption (E2EE) because the
                server is encrypting the files.</b
            >
        </p>
        <DropAndUrls />
    </v-container>
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
