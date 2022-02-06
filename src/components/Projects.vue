<template>
    <div>
        <p class="text-center text-h4 my-3">Projects</p>
        <HeaderUnderliner />
        <v-card elevation="0" color="transparent" class="text-center mx-auto" max-width="1250px">
            <v-container>
                <v-row dense>
                    <v-col cols="12">
                        <v-card class="pa-5">
                            <div
                                class="flex-no-wrap justify-space-between"
                                :class="$vuetify.breakpoint.lgAndUp ? 'd-flex' : ''"
                            >
                                <div>
                                    <v-card-subtitle class="text-h5">Speed Typer</v-card-subtitle>

                                    <v-card-subtitle>
                                        <v-chip
                                            color="blue-grey darken-1"
                                            class="ma-1"
                                            v-for="(tech, index) in speedTyperTechnologies"
                                            :key="index"
                                        >{{ tech }}</v-chip>
                                    </v-card-subtitle>

                                    <v-card-text>
                                        <div class="text--primary body-1">
                                            Speed Typer is a game that runs in a web browser. The idea is to type the words you as precisely as you can before timer runs out. The points are determined on how precisely you type the words. The game can be played at
                                            <a
                                                href="https://speed-typer-demo.herokuapp.com/"
                                                class="text-decoration-none"
                                            >https://speed-typer-demo.herokuapp.com/</a>.
                                        </div>
                                        <div class="text--primary mt-4 body-1">
                                            Application is divided into two repositories,
                                            <a
                                                href="https://github.com/RikuKukkaniemi/speed-typer-backend"
                                                class="text-decoration-none"
                                            >backend</a> and
                                            <a
                                                href="https://github.com/RikuKukkaniemi/speed-typer-frontend"
                                                class="text-decoration-none"
                                            >frontend</a>. Backend is a simple RESTful API made with Go and Gin. Backend communicates with MongoDB and frontend. Frontend is made with Laravel, Vue and Bootstrap stack. Both repositories are Dockerized. Backend runs in GCP and frontend in Heroku.
                                        </div>
                                    </v-card-text>
                                </div>
                                <div max-width="600">
                                    <v-img src="../assets/speed-typer-diagram.jpg"></v-img>
                                </div>
                            </div>
                        </v-card>
                    </v-col>
                </v-row>
                <v-row dense>
                    <v-col cols="12">
                        <v-card class="pa-5 mt-5">
                            <div>
                                <v-card-subtitle class="text-h5">My website</v-card-subtitle>

                                <v-card-subtitle>
                                    <v-chip color="blue-grey darken-1" class="ma-1">Vue</v-chip>
                                    <v-chip color="blue-grey darken-1" class="ma-1">Vuetify</v-chip>
                                </v-card-subtitle>

                                <v-card-text>
                                    <div
                                        class="text--primary body-1"
                                    >This is the website you are currently visiting at. It has been created by using Vue and Vuetify.</div>
                                    <div class="text--primary mt-4 body-1">
                                        The repository can be found here:
                                        <a
                                            href="https://github.com/RikuKukkaniemi/my-website"
                                            class="text-decoration-none"
                                        >https://github.com/RikuKukkaniemi/my-website</a>.
                                    </div>
                                </v-card-text>
                            </div>
                        </v-card>
                    </v-col>
                </v-row>
            </v-container>
        </v-card>
    </div>
</template>

<script>
import HeaderUnderliner from "./utility/HeaderUnderliner";

export default {
    components: {
        HeaderUnderliner,
    },
    data: () => ({
        speedTyperTechnologies: [
            'Go', 'Laravel', 'MongoDB', 'Vue.js', 'Bootstrap', 'Docker'
        ]
    }),
};
</script>
