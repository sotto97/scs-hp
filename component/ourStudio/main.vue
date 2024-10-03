<template>
  <div class="container">
    <lp-component></lp-component>
    <about-component></about-component>
    <!-- <artist-component></artist-component> -->
    <!-- <release-component></release-component> -->
    <!-- <faq-component></faq-component> -->
    <prompt-component></prompt-component>
    <qa-component></qa-component>
    <!-- <moc-component></moc-component> -->
  </div>
</template>

<script>
const LpComponent = httpVueLoader("./lp.vue");
const AboutComponent = httpVueLoader("./about.vue");
const ArtistComponent = httpVueLoader("./artist.vue");
const ReleaseComponent = httpVueLoader("./release.vue");
const PromptComponent = httpVueLoader("./prompt.vue");
const QaComponent = httpVueLoader("./qa.vue");
const FaqComponent = httpVueLoader("./faq.vue");
const MocComponent = httpVueLoader("./moc.vue");

module.exports = {
  components: {
    LpComponent,
    AboutComponent,
    ArtistComponent,
    ReleaseComponent,
    FaqComponent,
    PromptComponent,
    QaComponent,
    MocComponent,
  },
  name: "OurStudioComponent",
};
</script>
