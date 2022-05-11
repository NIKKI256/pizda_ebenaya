<template>
    <div>
        <h2>User {{ id }}</h2>
    </div>
</template>

<script>
export default {
    validate({ params }) {
        return /^\d+$/.test(params.id)
    },
    computed:{
        id() {
            return this.$route.params.id
        }
    }
}
</script>
