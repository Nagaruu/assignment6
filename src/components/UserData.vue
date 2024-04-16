<template>
    <form @submit.prevent="submitForm">
        <div>
            <label>Name</label>
            <input type="text" v-model='name'>
        </div>
        <div>
            <label>Age</label>
            <input type="text" v-model='age'>
        </div>
        <button>Add User</button>
    </form>
</template>
<script>
export default {
    data() {
        return {
            name : '',
            age: ''
        }
    },
    emits: [
        'submit-form'
    ],
    methods: {
        submitForm() {
            this.$emit('submit-form',this.name, this.age)
        }
    }
}
</script>
<style>
form {
    text-align: center;
}

#app {
    text-align: center;
}

ul {
  list-style-type: none;
}

</style>