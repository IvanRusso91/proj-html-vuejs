<template>
  <bosy>

    <HeaderComp/>

    <jumbotron-comp/>

    <main>

      <ServicesComp/>
      <CompanyComp/>
      <ProjectsComp/>
      <ResultsComp/>
      <TouchComp/>

    </main>

    <FooterComp/>
    
  </bosy>
</template>

<script>

import HeaderComp from "./components/HeaderComp.vue";
import JumbotronComp from "./components/JumbotronComp.vue";
import ServicesComp from "./components/ServicesComp.vue";
import CompanyComp from "./components/CompanyComp.vue";
import ProjectsComp from "./components/ProjectsComp.vue";
import ResultsComp from "./components/ResultsComp.vue";
import TouchComp from "./components/TouchComp.vue";
import FooterComp from "./components/FooterComp.vue";


export default {
  name: 'App',
  components: {
    HeaderComp,
    JumbotronComp,
    ServicesComp,
    CompanyComp,
    ProjectsComp,
    ResultsComp,
    TouchComp,
    FooterComp,
  }
}
</script>

<style lang="scss">

</style>
