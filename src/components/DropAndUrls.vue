<template>
    <div class="hello">
        <vue-dropzone
            ref="myVueDropzone"
            id="dropzone"
            :options="dropzoneOptions"
            @vdropzone-success-multiple="uploadSuccess"
            @vdropzone-processing="processing"
        />
        <ul>
            <li v-for="(url, i) in urls" :key="i">
                <a :href="url">{{ url }}</a>
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
import vue2Dropzone from "vue2-dropzone"
import "vue2-dropzone/dist/vue2Dropzone.min.css"
import Vue from "vue"
export default Vue.extend({
    components: {
        vueDropzone: vue2Dropzone,
    },
    data: () => ({
        dropzoneOptions: {
            paramName: "files",
            url: "https://server.dumpme.app/upload",
            thumbnailWidth: 150,
            maxFilesize: 10000,
            timeout: 9999999,
            uploadMultiple: true,
            headers: { "Cache-Control": null, "X-Requested-With": null },
            parallelUploads: 10,
        },
        urls: [] as string[],
    }),
    methods: {
        // eslint-disable-next-line @typescript-eslint/no-explicit-any
        uploadSuccess(file: File, response: any) {
            this.urls.push(response.url)
        },
    },
})
</script>

<style lang="sass" scoped></style>
