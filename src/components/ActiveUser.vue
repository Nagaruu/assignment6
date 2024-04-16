<template>
    <h2>{{ name }}</h2>
    <h3>{{ age }}</h3>
</template>
<script>
export default {
    props: {
        id: {
            type: String,
            require: false
        },
        name: {
            type: String,
            require: true
        },
        age: {
            type: String,
            require: true
        }
    }
}
</script>