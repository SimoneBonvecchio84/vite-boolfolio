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
        <h1 class="py-3">Lista Progetti</h1>
        <div class="row gap-2">
            <div class="col" v-for="curProject in projects ">
                <div class="card h-100" style="width: 18rem;">
                    <img src="..." class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">
                            {{ curProject.title }}
                        </h5>
                        <h5 class="card-title">
                            {{ curProject.type_id }}
                        </h5>

                        <p>
                            {{ curProject.content }}
                        </p>

                        <h6>Data:
                            {{ curProject.created_at }}
                        </h6>
                      
                    </div>
                </div>

            </div>
        </div>
    </div>


</template>

<style lang="scss" scoped></style>