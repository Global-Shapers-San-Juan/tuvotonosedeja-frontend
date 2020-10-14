<template>
  <div>
    <NavBar />
    <CandidateCardLoading v-if="$apollo.loading" />
    <div v-else>
      <CandidateCard
        v-for="candidato in senados"
        :key="candidato.id"
        :candidate-name="candidato.nombre"
        :candidate-profile-pic="candidato.profile_img.formats.thumbnail.url"
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
import senadoresQuery from '../apollo/queries/candidatos/senadores.gql'

export default {
  components: {
    CandidateCard,
    CandidateCardLoading,
    NavBar,
  },
  data() {
    return {
      senados: [],
      loading: 0,
      error: null,
    }
  },
  apollo: {
    $loadingKey: 'loading',
    senados: {
      prefetch: true,
      query: senadoresQuery,
    },
  },
}
</script>

<style></style>
