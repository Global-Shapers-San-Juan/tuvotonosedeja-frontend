<template>
  <div>
    <b-list-group>
      <b-list-group-item class="d-flex align-items-center">
        <div class="row">
          <b-col cols="4">
            <b-avatar v-if="$apollo.loading" class="mr-3" size="4em"></b-avatar>
            <b-avatar
              v-else
              class="remove-bg"
              size="4.5em"
              :src="candidateProfilePic"
            ></b-avatar>
          </b-col>
          <b-col cols="8" class="mr-auto nombre-title">
            <div class="row">
              {{ candidateName }}
            </div>
            <div class="row puesto-subtitle">
              {{ candidatePosition }}
            </div>
            <div class="row mt-2">
              <b-badge
                v-if="candidatePartyColor === '5'"
                class="partido-tag"
                variant="primary"
                >{{ candidateParty }}</b-badge
              >
              <b-badge
                v-if="candidatePartyColor === '4'"
                class="partido-tag"
                variant="success"
                >{{ candidateParty }}</b-badge
              >
              <b-badge
                v-if="candidatePartyColor === '3'"
                class="partido-tag"
                variant="danger"
                >{{ candidateParty }}</b-badge
              >
              <b-badge
                v-if="candidatePartyColor === '2'"
                class="partido-tag"
                variant="info"
                >{{ candidateParty }}</b-badge
              >
              <b-badge
                v-if="candidatePartyColor === '1'"
                class="partido-tag"
                variant="warning"
                >{{ candidateParty }}</b-badge
              >
              <b-badge
                v-if="candidatePartyColor === '6'"
                class="partido-tag"
                variant="secondary"
                >{{ candidateParty }}</b-badge
              >
            </div>
          </b-col>
        </div>
      </b-list-group-item>
    </b-list-group>
  </div>
</template>

<script>
export default {
  name: 'CandidateCard',
  props: {
    candidateName: {
      type: String,
      default: '',
    },
    candidatePosition: String,
    candidateParty: {
      type: String,
      default: '',
    },
    candidateProfilePic: {
      type: String,
      default: '',
    },
    candidatePartyColor: String,
  },
}
</script>

<style>
.partido-tag {
  font-size: 8px;
}
.nombre-title {
  font-weight: bold;
  font-size: 14px;
}
.puesto-subtitle {
  font-size: 12px;
  font-weight: normal;
}
.remove-bg {
  background-color: white;
}
</style>
