<script>
import axios from 'axios';
import ProjectCard from '../ProjectCard.vue'

export default {
    components: {
        ProjectCard,
    },
    data() {
        return {
            // variabile da riempire con axios
            projects: [],
        }
    },
    created() {
        axios.get("http://127.0.0.1:8000/api/projects").then((resp) => {
            // salvo i dati nella varibile iniziale
            this.projects = resp.data.projects;
            // console.log(this.projects);
        })
    }
}
</script>

<template>
    <h1 class="text-center py-4">Projects</h1>

    <div class="container">
        <div class="row">
            <div class="col-3" v-for="project in projects" :key="project.id">
                <router-link class="text-decoration-none" :to="{ name:'show-project', params:{ slug: project.slug }}">
                    <ProjectCard :project="project" />
                </router-link>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.col-3 > * {
    aspect-ratio: 0.5;
}
</style>