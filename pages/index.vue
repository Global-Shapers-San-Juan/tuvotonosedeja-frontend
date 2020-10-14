<template>
  <div>
    <NavBar />
    <div>
      <b-tabs content-class="mt-3" fill>
        <b-tab title="Sobre Nosotros" active class="p-2">
          <b-card class="text-center">
            <img src="~/assets/logo.png" alt="" class="mb-3" />
            <b-card-text>
              Tu Voto No Se Deja surge a raíz del deseo de la ACLU de Puerto
              Rico de empoderar al pueblo por medio de la educación electoral;
              nuestro enfoque es proveer información para que quien decida
              llevar a cabo su derecho al voto, lo haga con conocimiento.
            </b-card-text>
          </b-card>
        </b-tab>
        <b-tab title="ACLU Puerto Rico" class="p-2">
          <b-card class="text-center">
            <img src="~/assets/aclupr.png" alt="" class="mb-3" />
            <b-card-text>
              ACLU de Puerto Rico es una organización no sectaria, sin fines de
              lucro cuyo propósito es adelantar los derechos civiles,
              constitucionales y humanos de todas las personas. Nuestro interés
              principal es que a través de nuestro esfuerzo se ayude a
              establecer una política pública robusta que promueva la protección
              de derechos humanos fundamentales para todas las personas, el
              respeto a la diversidad, la participación comunitaria en la toma
              de decisiones y abrir el acceso a la justicia a los sectores
              tradicionalmente desaventajados.
            </b-card-text>
          </b-card>
        </b-tab>
        <b-tab title="Global Shapers San Juan" class="p-2">
          <b-card class="text-center">
            <img src="~/assets/globalshapersj.png" alt="" class="mb-3" />
            <b-card-text>
              Global Shapers es una red global de jóvenes que promueven diálogo,
              acción y cambio en sus comunidades. El San Juan Hub es compuesto
              por 32 jóvenes de diversos trasfondos profesionales. En
              colaboración con la ACLU lanzaron esta página para lograr que más
              jóvenes aprendan sobre las plataformas de los candidatos antes de
              votar.
            </b-card-text>
          </b-card>
        </b-tab>
        <b-tab title="Otros Enlances">
          <ul>
            <li>Facebook</li>
            <li>Twitter</li>
            <li>Instagram</li>
            <li>Para Votar</li>
            <li>¿Quién me representa?</li>
          </ul>
        </b-tab>
      </b-tabs>
    </div>
    <div class="container p-4 text-center">
      <h3>Ver Perfiles de Candidatxs</h3>
      <div>
        <b-button href="/gobernacion" pill variant="light m-2"
          >Gobernación</b-button
        >
      </div>
      <div>
        <b-button href="/senado" pill variant="light m-2">Senado</b-button>
      </div>
      <div>
        <b-button href="/representantes" pill variant="light m-2"
          >Cámara de Representantes</b-button
        >
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from '../components/NavBar'

export default {
  components: {
    NavBar,
  },
  data() {
    return {}
  },
  apollo: {},
}
</script>

<style></style>
