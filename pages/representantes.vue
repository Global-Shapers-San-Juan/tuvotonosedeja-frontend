<template>
  <div>
    <NavBar />
    <CandidateCard
      v-for="candidato in representantes"
      :key="candidato.id"
      :candidate-name="candidato.nombre"
      :candidate-profile-pic="candidato.profile_img[0].url"
      :candidate-party="candidato.partido.partido_titulo"
      :candidate-position="candidato.puesto"
      :candidate-party-color="candidato.partido.id"
    />
  </div>
</template>

<script>
import NavBar from '../components/Navbar'
import CandidateCard from '../components/CandidateCard'
import representantesQuery from '../apollo/queries/candidatos/representantes.gql'

export default {
  components: {
    CandidateCard,
    NavBar,
  },
  data() {
    return {
      representantes: [],
      loading: 0,
      error: null,
    }
  },
  apollo: {
    $loadingKey: 'loading',
    representantes: {
      prefetch: true,
      query: representantesQuery,
    },
  },
}
</script>

<style></style>
