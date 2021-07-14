<template>
  <div class="student_id">
    <div>
      <h1>{{student.name}}</h1>
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink> | <NuxtLink to="/">トップページへ</NuxtLink>
    </div>
  </div>
</template>


<script>
export default {
  validate({ params }) {
    if(params.id === undefined){
      return false
    } else {
      return true
    }
  },
  data() {
    return {
      id: this.$route.params.id,
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
  computed: {
    student() {
        return this.students.find(student => student.id == this.id);
    }
  },
};
</script>


<style>
.student_id {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>


