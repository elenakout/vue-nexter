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

  & > * {
    padding: 40px;
    font-size: 3rem;
  }
}

.features {
  background-color: cornflowerblue;
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
}

.story__pictures {
  background-color: greenyellow;
  grid-column: full-start / col-end 4;
}
</style>
