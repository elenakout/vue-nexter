<template>
  <div class="nexter-project">
    <div class="container">
      <div class="sidebar">
        <sidebar />
      </div>

      <header class="header">
        <Header />
      </header>

      <div class="realtors">
        <realtors />
      </div>

      <section class="features">
        <features />
      </section>

      <div class="story__pictures">
        <story-pictures />
      </div>

      <div class="story__content">
        <story-content />
      </div>

      <section class="homes">
        <homes />
      </section>

      <section class="gallery">
        <gallery />
      </section>

      <footer class="footer">
        <Footer />
      </footer>
    </div>
  </div>
</template>

<script>
import Header from "@/components/nexter/_header.vue";
import Sidebar from "@/components/nexter/_sidebar.vue";
import Features from "@/components/nexter/_features.vue";
import Footer from "@/components/nexter/_footer.vue";
import Gallery from "@/components/nexter/_gallery.vue";
import Homes from "@/components/nexter/_homes.vue";
import Realtors from "@/components/nexter/_realtors.vue";
import StoryContent from "@/components/nexter/_story-content.vue";
import StoryPictures from "@/components/nexter/_story-pictures.vue";

export default {
  name: "nexter",
  components: {
    Header,
    Sidebar,
    Features,
    Footer,
    Gallery,
    Homes,
    Realtors,
    StoryContent,
    StoryPictures
  }
};
</script>

<style lang="scss">
.nexter-project {
  font-family: var(--font-primary);
  color: var(--color-grey-dark-2);
  font-weight: 300;
  line-height: 1.6;
}

.container {
  display: grid;
  grid-template-rows: 80vh min-content 40vw repeat(3, min-content);
  grid-template-columns:
    [sidebar-start] 8rem [sidebar-end full-start] minmax(6rem, 1fr)
    [center-start] repeat(8, [col-start] minmax(min-content, 14rem) [col-end])
    [center-end] minmax(6rem, 1fr)
    [full-end];
}

.features {
  grid-column: center-start / center-end;
}

.footer {
  background-color: var(--color-secondary);
  grid-column: full-start / full-end;
}

.gallery {
  background-color: khaki;
  grid-column: full-start / full-end;
}

.header {
  background-color: aquamarine;
  grid-column: full-start / col-end 6;
}

.homes {
  background-color: burlywood;
  grid-column: center-start / center-end;
}

.realtors {
  background-color: var(--color-secondary);
  grid-column: col-start 7 / full-end;
}

.sidebar {
  background-color: var(--color-primary);
  grid-column: sidebar-start / sidebar-end;
  grid-row: 1 / -1;
}

.story__content {
  background-color: var(--color-grey-light-1);
  grid-column: col-start 5 / full-end;
  padding: 6rem 8vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.story__pictures {
  grid-column: full-start / col-end 4;
}

// TYPOGRAPHY
%heading {
  font-family: var(--font-display);
  font-weight: 400;
}

.heading-1 {
  @extend %heading;
}

.heading-2 {
  @extend %heading;
  font-size: 4rem;
  font-style: italic;
  line-height: 1;

  &--light {
    color: var(--color-grey-light-1);
  }
  &--dark {
    color: var(--color-grey-dark-1);
  }
}

.heading-3 {
  @extend %heading;
  font-size: 1.6rem;
  color: var(--color-primary);
  text-transform: uppercase;
}

.heading-4 {
  @extend %heading;
  font-size: 1.9rem;

  &--light {
    color: var(--color-grey-light-1);
  }
  &--dark {
    color: var(--color-grey-dark-1);
  }
}

// BUTTON
.btn {
  background-color: var(--color-primary);
  color: #fff;
  border: none;
  border-radius: 0;
  font-family: var(--font-display);
  font-size: 1.5rem;
  text-transform: uppercase;
  padding: 1.8rem 3rem;
  cursor: pointer;
  transition: all 0.2s;

  &:hover {
    background-color: var(--color-primary-dark);
  }
}

// MARGINS
.mb-sm {
  margin-bottom: 2rem;
}
.mb-md {
  margin-bottom: 3rem;
}
.mb-lg {
  margin-bottom: 4rem;
}
.mb-hg {
  margin-bottom: 8rem;
}
</style>
