<template>
    <v-app>
        <v-app-bar
                app
                color="white"
                elevation="2"
        >
            <div class="d-flex align-center">
                <v-img
                        alt="Vuetify Logo"
                        class="shrink mr-2"
                        contain
                        src="./assets/logo.png"
                        transition="scale-transition"
                        width="40"
                />
            </div>
            <v-toolbar-title>IIT JEE Notes by Ayush P Gupta</v-toolbar-title>


            <v-spacer></v-spacer>
            <v-btn
                    href="https://unacademy.com/@ayushpgupta"
                    target="_blank"
                    text
            >
                <span class="mr-2 hidden-xs-only">Unacademy</span>
                <v-icon>mdi-open-in-new</v-icon>
            </v-btn>

        </v-app-bar>

        <v-content>
            <router-view/>
        </v-content>
        <v-footer class="px-4 py-1" color="primary" dark padless fixed>
            <div>&copy; {{ new Date().getFullYear() }}</div>


            <a class="white--text ml-2" href="https://apgapg.github.io/" target="_blank">Ayush P Gupta</a>


            <v-spacer/>
            <v-btn color="white" href="https://github.com/apgapg" icon small target="_blank" text>
                <v-icon size="20">mdi-github-circle</v-icon>
            </v-btn>
            <v-btn color="white" href="https://www.linkedin.com/in/ayushpgupta/" icon small target="_blank" text>
                <v-icon size="20">mdi-linkedin</v-icon>
            </v-btn>

            <v-btn color="white" href="https://www.facebook.com/ayushpgupta" icon small target="_blank" text>
                <v-icon size="20">mdi-facebook-box</v-icon>
            </v-btn>
        </v-footer>
    </v-app>
</template>

<script>

export default {
    name: 'App',

    components: {},

    data: () => ({
        //
    }),
};
</script>
