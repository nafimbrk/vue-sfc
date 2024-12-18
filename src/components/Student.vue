<template>
    <slot>ini adalah slot default karena parent component tidak memberikan data</slot> <br>
    ini adalah data dari siswa yg bernama {{ studentName }} <button @click="showData">show detail</button> <br>
</template>

<script>
export default {
    props: {
        studentName: String
    },
    emits: ['response'],
    methods: {
        showData() {
            this.$emit('response', this.studentName)
        }
    }
}
</script>