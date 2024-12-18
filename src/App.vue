<template>
  <Student @response="showData" studentName="andi">ini adalah nilai slot dari parent</Student> <br>
  <Student @response="showData" studentName="budi"></Student> <br>
  <Student @response="showData" studentName="ani"></Student>

  <p>
    student yg dipilih adalah: {{ selectedStudent }}
  </p>
</template>

<script>
import Student from './components/Student.vue';

export default {
  components: {
    Student
  },
  data() {
    return {
      selectedStudent: ''
    }
  },
  methods: {
    showData(whatever) {
      this.selectedStudent = whatever
    }
  }
}
</script>