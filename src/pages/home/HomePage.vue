<template>
    <v-container class="pb-8">
        <p class="pt-2 body-1 text-center">Hello Aspirant! Here's the compilation of all the videos for IIT JEE
                                           PHYSICS</p>
        <p class="pb-0 body-1 text-center">Made with ❤️ by Ayush P Gupta</p>
        <v-row align="stretch">
            <v-col :key="i" cols="12" md="4" v-for="(course,i) in courses">
                <v-card :to="{name:'course', params: {courseId:course.id}}" style="height: 270px;">
                    <v-container>
                        <v-card-title>{{course.title}}</v-card-title>
                        <v-card-text class="text-wrap">
                            {{course.description}}
                        </v-card-text>
                    </v-container>
                </v-card>
            </v-col>
        </v-row>
        <v-container>
            <v-card outlined>
                <v-container>
                    <p class="pt-2 body-1 text-center">View my other Physics-Concept website for better visual understanding</p>
                    <v-container class="d-flex justify-center"  >
                        <v-btn color="primary" href="https://physics-concepts.firebaseapp.com/" target="_blank" outlined>VISIT WEBSITE</v-btn>
                    </v-container>
                </v-container>
            </v-card>

        </v-container>
    </v-container>
</template>

<script>
import {courses} from './config';

export default {
    name: 'home-page',

    data: () => ({
        courses: courses
    }),
};
</script>
