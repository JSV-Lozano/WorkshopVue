<script setup>
import { defineProps } from "vue";
import empresa from "../../assets/bx-buildings.svg";
defineProps({
  job: Object,
});
</script>
<template>
  <div class="container_CardJobs">
    <div class="cardJobs">
      <div class="logo">
        <img
          :src="job.logo"
          alt="logo"
        />
      </div>
      <div class="infoJobs">
        <div class="conatiner_Title">
          <h2 class="text-primary">{{ job.title }}</h2>
          <div
            v-for="skill in job.skills"
            :key="job.id"
          >
            <p>
              {{ skill.name }}
            </p>
          </div>
        </div>
        <section class="jobsInfo">
          <div class="Info">
            <img
              :src="job.logoEmpresa"
              :alt="job.name"
            />
            <p>{{ job.empresa }}</p>
          </div>
          <div class="Info">
            <img
              :src="job.logoUbi"
              alt="tipo de empleo"
            />
            <p>{{ job.ubicacion }}</p>
          </div>
          <div class="Info">
            <img
              :src="job.logoPago"
              alt="pago"
            />
            <p>{{ job.pago }}</p>
          </div>
          <div class="Info">
            <img
              :src="job.logoVacante"
              alt="vacantes"
            />
            <p>{{ job.vacantes }}</p>
          </div>
          <div class="Info">
            <img
              :src="job.logoPublicado"
              alt="publicado"
            />
            <p>{{ job.publicado }}</p>
          </div>
          <div class="empreOfr">
            <img
              v-for="emp in job.empresaOfrece"
              :src="emp.logo"
              alt=""
            />
          </div>
        </section>
      </div>
    </div>
  </div>
</template>
