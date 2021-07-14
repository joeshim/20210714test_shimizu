<template>
  <div class="students">
    <div>
      <h1>生徒一覧</h1>
      <li v-for="student in students" :key="student.name">
        <a v-bind:href="'students/' + student.id">{{student.name}}</a>
      </li>
      <NuxtLink to="/">戻る</NuxtLink>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
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
};
</script>


<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>