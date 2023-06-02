<template>
  <main :class="[$route.name]" class="main px-4 md:px-0">
    <div class="w-full header">
      <site-header />
    </div>
    <div>
      <nuxt class="container mx-auto nuxt" />
    </div>
    <svg class="divider -mx-4 sm:mx-0" width="100%" viewBox="0 0 10 1">
      <polygon stroke="none" stroke-width="0" fill="#53c3c2" points="0,0.6 0,1 10,1 10,0" />
    </svg>

    <site-footer />
  </main>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import SiteHeader from '@/components/partials/header.vue';
import SiteFooter from '@/components/partials/footer.vue';

@Component({
  components: {
    SiteHeader,
    SiteFooter,
  },
})
export default class DefaultLayout extends Vue {}
</script>
