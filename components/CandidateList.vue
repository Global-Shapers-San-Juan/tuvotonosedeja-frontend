<template>
  <div>
    <CandidateCard
      v-for="candidato in candidatoes"
      :key="candidato.id"
      :candidate-name="candidato.nombre"
      :candidate-party="candidato.partido.partido_titulo"
      candidate-position="Candidata a la Gobernacion"
      :candidate-profile-pic="candidato.profile_img.url"
      candidate-party-color="warning"
    />
  </div>
</template>

<script>
import CandidateCard from '../components/CandidateCard'

export default {
  components: {
    CandidateCard,
  },
  props: {
    candidatoes: {
      type: Array,
      default: () => [],
    },
  },
}
</script>

<style></style>
