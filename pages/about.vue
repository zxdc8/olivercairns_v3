<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      image="/uploads/paragliding_hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>About Me</h3>
          <p>
            I'm Ollie. I'm a final year Aerospace Engineering student at the university of Bristol and am fascinated by anything that flies, drives, floats or orbits. Here is a collection of my projects and anything else I'm interested in.
          </p>
        </div>

        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Cool Stuff We Do
              </p>
              <p class="subtitle">
                Sooo Cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Other Cool Things
              </p>
              <p class="subtitle">
                Just as cool
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                All the cool
              </p>
              <p class="subtitle">
                that is all
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
		<div class="tile is-parent is-8">
				<article class="tile is-child box">
				<contact-form />
				</article>
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>

<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>