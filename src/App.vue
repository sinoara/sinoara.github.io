<template>
    <v-app id="inspire">
        <v-app-bar flat>
            <v-container class="mx-auto d-flex align-center justify-center">
                <v-avatar class="me-4 " color="grey-darken-1" size="32"></v-avatar>

                <v-btn v-for="link in links" :key="link" :text="link" variant="text"></v-btn>

                <!--
                <v-spacer></v-spacer>

                <v-responsive max-width="160">
                    <v-text-field density="compact" label="Search" rounded="lg" variant="solo-filled" flat hide-details
                        single-line></v-text-field>
                </v-responsive>
                -->
            </v-container>
        </v-app-bar>

        <v-main class="bg-grey-lighten-3">
            <v-container>
                <v-row>
                    <v-col cols="auto" class="d-flex justify-center">
                        <v-sheet rounded="lg" class="d-flex justify-center align-center">
                            <v-list rounded="lg" class="justify-center">
                                <v-list-item>
                                    <v-avatar class="mx-2 my-2" color="grey-darken-1" size="160">
                                        <v-img src="./assets/profile_pic.png"></v-img>
                                    </v-avatar>
                                </v-list-item>

                                <v-divider class="my-2"></v-divider>

                                <v-list-item v-for="n in 5" :key="n" :title="`List Item ${n}`" link></v-list-item>

                                <v-divider class="my-2"></v-divider>

                                <v-list-item color="grey-lighten-4" title="Refresh" link></v-list-item>
                            </v-list>
                        </v-sheet>
                    </v-col>

                    <v-col>
                        <v-sheet min-height="70vh" rounded="lg">
                            <router-view />
                            <!--  -->
                        </v-sheet>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
    </v-app>
</template>

<script setup lang="ts">
const links = [
    'Dashboard',
    'Messages',
    'Profile',
    'Updates',
]
</script>

<script lang="ts">
export default {
    data: () => ({
        links: [
            'Dashboard',
            'Messages',
            'Profile',
            'Updates',
        ],
    }),
}
</script>
