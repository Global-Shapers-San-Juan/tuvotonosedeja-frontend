<template>
  <div>
    <NavBar />
    <CandidateCardLoading v-if="$apollo.loading" />
    <div v-else>
      <CandidateCard
        v-for="candidato in candidatoes"
        :key="candidato.id"
        :candidate-name="candidato.nombre"
        :candidate-profile-pic="candidato.profile_img.formats.thumbnail.url"
        :candidate-party="candidato.partido.partido_titulo"
        candidate-position="Candidata a la Gobernacion"
        :candidate-party-color="candidato.partido.id"
      />
    </div>
  </div>
</template>

<script>
import NavBar from '../components/Navbar'
import CandidateCard from '../components/CandidateCard'
import CandidateCardLoading from '../components/CandidateCardLoading'
import candidatosQuery from '../apollo/queries/candidatos/gobernadores.gql'

export default {
  components: {
    CandidateCard,
    CandidateCardLoading,
    NavBar,
  },
  data() {
    return {
      candidatoes: [],
      loading: 0,
      error: null,
    }
  },
  apollo: {
    $loadingKey: 'loading',
    candidatoes: {
      prefetch: true,
      query: candidatosQuery,
    },
  },
}
</script>

<style></style>
