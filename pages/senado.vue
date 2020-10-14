<template>
  <div>
    <NavBar />
    <CandidateCard
      v-for="candidato in senados"
      :key="candidato.id"
      :candidate-name="candidato.nombre"
      :candidate-profile-pic="candidato.profile_img.url"
      :candidate-party="candidato.partido.partido_titulo"
      :candidate-position="candidato.puesto"
      :candidate-party-color="candidato.partido.id"
    />
  </div>
</template>

<script>
import NavBar from '../components/Navbar'
import CandidateCard from '../components/CandidateCard'
import senadoresQuery from '../apollo/queries/candidatos/senadores.gql'

export default {
  components: {
    CandidateCard,
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
