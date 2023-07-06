<script setup>
import db from "../../db.json";
import ListJobs from "./ListJobs.vue";
import jobsList from "../../styles/jobsList.css";
</script>
<template>
  <div class="container_ListJobs">
    <ListJobs
      v-for="jobs in db.jobs"
      :key="jobs.id"
      :job="jobs"
    ></ListJobs>
  </div>
</template>
