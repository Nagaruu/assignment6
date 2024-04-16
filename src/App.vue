<template>
    <header>
    <h1>My Users</h1>
    </header>
    <user-data
        @submit-form="addUser"
    ></user-data>
    <ul v-for="user in users" :key="user.id">
        <li>
            <active-user
                :id="user.id"
                :name="user.name"
                :age="user.age"
            >
            </active-user>
        </li>
    </ul>
</template>
<script>
export default {
    data() {
        return {
            users : [
                {
                    id: '1',
                    name: 'Hoa',
                    age: '30'
                },
                {
                    id: '2',
                    name: 'Chuong',
                    age: '29'
                }
            ]
        }
    },
    methods: {
        addUser(name, age) {
            const newUser = {
                id: new Date().toISOString,
                name: name,
                age: age
            }
            
            this.users.push(newUser);
        }
    }
}
</script>