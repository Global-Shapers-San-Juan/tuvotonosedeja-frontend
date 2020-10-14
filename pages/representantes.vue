<template>
  <div>
    <NavBar />
    <CandidateCardLoading v-if="$apollo.loading" />
    <div v-else>
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
  </div>
</template>

<script>
import NavBar from '../components/Navbar'
import CandidateCard from '../components/CandidateCard'
import CandidateCardLoading from '../components/CandidateCardLoading'
import representantesQuery from '../apollo/queries/candidatos/representantes.gql'

export default {
  components: {
    CandidateCard,
    CandidateCardLoading,
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
