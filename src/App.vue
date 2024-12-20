<!-- <template>
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
</script> -->

<template>
  <div class="menu">
    <Navbar />
  </div>

  <div class="main">
    <RouterView />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
  components: {
    Navbar
  }
}
</script>

<style>
body {
   margin: 0;
}
</style>

<style scoped>
.menu {
  background-color: #eee;
  line-height: 2;
  padding: 10px;
}

.main {
  padding: 10px;
}
</style>