<script>
import axios from 'axios';
export default {
    data() {
        return {
            projects: []
        }
    },
    created() {
        axios.get('http://127.0.0.1:8000/api/projects').then((resp) => {
            console.log(resp);
            this.projects = resp.data.result;
        })
    }
}
</script>

<template>
    <div class="container">
        <h1>Lista Progetti</h1>
        <div class="row">
            <div class="col" v-for="curProject in projects ">
                <div class="card">
                    <h4>Titolo</h4>
                    {{ curProject.title }}
                    <h5>Tipologia</h5>
                    {{ curProject.type_id }}
                </div>
            </div>
        </div>
    </div>


</template>

<style lang="scss" scoped></style>