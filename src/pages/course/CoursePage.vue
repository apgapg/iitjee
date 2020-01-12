<template>
    <v-container>
        <p class="title text-center mb-0 pb-0" v-if="lessons && lessons.length>0">Total Lessons: {{lessons.length}}</p>
        <v-container class="d-flex justify-center">
            <v-list v-if="lessons && lessons.length>0">
                <div :key="i" cols="12" md="12" v-for="(lesson,i) in lessons">
                    <v-container>
                        <v-card outlined>
                            <v-container>
                                <iframe :src="'https://unacademy.com/embed/'+lesson" allowfullscreen frameborder="0"
                                        height="315"
                                        style="min-width:560px;min-height:315px;" width="560"></iframe>
                                <p class="mb-0 pb-0">Lesson {{i+1}}</p>

                            </v-container>
                        </v-card>
                    </v-container>
                </div>

            </v-list>
            <v-container v-else>
                <div class="d-flex justify-center mb-4">
                    <v-icon size="40">mdi-emoticon-happy-outline</v-icon>
                </div>
                <v-container class="d-flex justify-center">
                    <p>Course will be uploaded soon. Meanwhile you can visit unacademy and watch the lessons there.</p>
                </v-container>
                <v-container class="d-flex justify-center"  >
                    <v-btn color="primary" :href="link" target="_blank" outlined>VIEW ON UNACADEMY</v-btn>
                </v-container>
            </v-container>
        </v-container>
    </v-container>

</template>

<script>
import {courses} from './config';

export default {
    name: 'course-page',

    data: () => ({
        courses: courses
    }),
    computed: {
        lessons() {
            return courses[this.$route.params.courseId];
        },
        link() {
            return 'https://unacademy.com/course/' + this.$route.params.courseId;
        }
    },
    mounted() {
        // console.log(this.$route.params.courseId)
    }
};
</script>
