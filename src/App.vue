<template>
    <v-app>
        <v-app-bar app color="primary" dark>
            <v-toolbar-title>Dump Me</v-toolbar-title>
            <v-app-bar-nav-icon
                ><v-icon>fas fa-dumpster</v-icon></v-app-bar-nav-icon
            >
            <v-spacer></v-spacer>
            <v-app-bar-nav-icon
                href="https://github.com/therealpaulgg/dumpme-server"
                target="_blank"
                ><v-icon>fab fa-github</v-icon></v-app-bar-nav-icon
            >
        </v-app-bar>

        <v-content>
            <router-view />
        </v-content>
    </v-app>
</template>

<script lang="ts">
import Vue from "vue"

export default Vue.extend({
    name: "App",

    data: () => ({
        //
    }),
})
</script>
