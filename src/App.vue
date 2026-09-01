<template>
    <v-app id="inspire">
        <!--
        <v-app-bar flat>
            <v-container class="mx-auto d-flex align-center justify-center">
                <v-avatar class="me-4 " color="grey-darken-1" size="32"></v-avatar>

                <v-btn v-for="link in links" :key="link" :text="link" variant="text"></v-btn>
            </v-container>
        </v-app-bar>
        -->

        <v-main class="bg-grey-lighten-3">
            <v-container>
                <v-row>
                    <v-col cols="auto" class="d-flex justify-center">
                        <v-sheet rounded="lg" class="d-flex justify-center align-center">
                            <v-list rounded="lg" class="justify-center">
                                <v-list-item>
                                    <v-avatar class="mx-2 my-2" color="grey-darken-1" size="200">
                                        <v-img src="./assets/profile_pic.png"></v-img>
                                    </v-avatar>
                                </v-list-item>

                                <v-list-item>
                                    <v-card title="Guilherme Sinoara" subtitle="Engenheiro Aeronáutico">
                                    </v-card>
                                </v-list-item>
                                <v-list-item>
                                    <div class="d-flex w-50">
                                        <v-chip class="ml-1 mb-1" density="compact" v-for="skill in skills">{{ skill
                                        }}</v-chip>
                                    </div>
                                </v-list-item>

                                <v-divider class="my-2"></v-divider>

                                <v-list-item title="Experiência profissional" link></v-list-item>
                                <v-list-item title="Educação" link></v-list-item>
                                <v-list-item title="Projetos" link></v-list-item>


                                <v-divider class="my-2"></v-divider>

                                <v-list-item color="grey-lighten-4" title="Currículo (pdf)" link></v-list-item>
                            </v-list>
                        </v-sheet>
                    </v-col>

                    <v-col>
                        <v-sheet class="overflow-y-auto" min-height="95vh" rounded="lg">
                            <router-view />
                        </v-sheet>
                    </v-col>
                </v-row>
            </v-container>
        </v-main>
    </v-app>
</template>

<script setup lang="ts">
const skills: string[] = [
    'Python',
    'Django',
    'Git',
    'Dart(Flutter)',
    'PyTorch',
    'Machine Learning',
    'Linux',
    'Pacote Office',
    'MATLAB',
    'Simulink',
    'Arduino',
    'Latex',
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
