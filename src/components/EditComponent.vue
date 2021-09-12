<template>
    <div class="row justify-content-center">
        <div class="col-md-6">
            <div class="card">
                <div class="card-header">
                    <h3 class="text-center display-6">Update Student</h3>
                </div>
                <div class="card-body">
                    <form @submit.prevent="handleUpdateForm">
                        <div class="form-group" style="padding-bottom: 10px">
                            <h4 class="lead">Name</h4>
                            <input type="text" class="form-control" v-model="student.name" required>
                        </div>

                        <div class="form-group" style="padding-bottom: 10px">
                            <h4 class="lead">Email</h4>
                            <input type="email" class="form-control" v-model="student.email" required>
                        </div>

                        <div class="form-group" style="padding-bottom: 10px">
                            <h4 class="lead">Phone</h4>
                            <input type="text" class="form-control" v-model="student.phone" required>
                        </div>

                        <div class="form-group text-center">
                            <button class="btn btn-primary btn-block">Update</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import axios from "axios";

    export default {
        data() {
            return {
                student: {}
            }
        },
        created() {
            let apiURL = `http://localhost:4000/api/edit-student/${this.$route.params.id}`;

            axios.get(apiURL).then((res) => {
                this.student = res.data;
            })
        },
        methods: {
            handleUpdateForm() {
                let apiURL = `http://localhost:4000/api/update-student/${this.$route.params.id}`;

                axios.put(apiURL, this.student).then((res) => {
                    console.log(res)
                    this.$router.push('/view')
                }).catch(error => {
                    console.log(error)
                });
            }
        }
    }
</script>