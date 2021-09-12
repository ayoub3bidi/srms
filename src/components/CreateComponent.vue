<template>
    <div class="row justify-content-center">
        <div class="col-md-6">
            <div class="card">
                <div class="card-header">
                    <h3 class="text-center display-6">Create Student</h3>
                </div>
                <div class="card-body">
                    <form @submit.prevent="handleSubmitForm">
                        <div style="padding-bottom: 10px;" class="form-group">
                            <input type="text" class="form-control" placeholder="Student name" v-model="student.name" required>
                        </div>

                        <div style="padding-bottom: 10px;" class="form-group">
                            <input type="email" class="form-control" placeholder="Student email" v-model="student.email" required>
                        </div>

                        <div style="padding-bottom: 10px;" class="form-group">
                            <input type="text" class="form-control" placeholder="Student phone number" v-model="student.phone" required>
                        </div>

                        <div class="form-group text-center">
                            <button class="btn btn-outline-success">Create</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                student: {
                    name: '',
                    email: '',
                    phone: ''
                }
            }
        },
        methods: {
            handleSubmitForm() {}
        }
    }
</script>