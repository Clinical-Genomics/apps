<template>
  <div id="app">
    <section class="section">
      <div class="section-body">
        <div class="grid">
          <div class="grid-item" v-for="app in apps">
            <Tool :id="app.id" :title="app.title" :subtitle="app.subtitle" :url="app.url" />
          </div>
        </div>
      </div>
    </section>

    <PageFooter />
  </div>
</template>

<script>
import PageFooter from './components/PageFooter.vue'
import Tool from './components/Tool.vue'

export default {
  data () {
    return {
      apps: [{
        'id': 'clinicaladmin',
        'title': 'Clinical Admin',
        'subtitle': 'Admin interface for customer data.',
        'url': 'http://trailblazer.clinicalgenomics.se:8082/'
      }, {
        'id': 'supportsystem',
        'title': 'Support System',
        'subtitle': 'Ticket system and customer contact',
        'url': 'https://clinical-scilifelab.supportsystem.com/scp/login.php'
      }, {
        'id': 'amsystem',
        'title': 'AM System',
        'subtitle': 'Quality assutance document system',
        'url': 'https://jo812.amsystem.com/index.php'
      }, {
        'id': 'orderform',
        'title': 'Orderform',
        'subtitle': 'Check validity of orderforms',
        'url': 'http://orderform.clinicalgenomics.se/'
      }, {
        'id': 'lims',
        'title': 'Clarity LIMS',
        'subtitle': 'Lab management system',
        'url': 'https://clinical-lims.scilifelab.se/clarity/'
      }, {
        'id': 'clinstatsdb',
        'title': 'Clinstats DB',
        'subtitle': 'QC tool for sequencing data',
        'url': 'https://clinical-db.scilifelab.se:8085/'
      }, {
        'id': 'trailblazer',
        'title': 'Trailblazer',
        'subtitle': 'Analysis manager and dashboard',
        'url': 'http://trailblazer.clinicalgenomics.se/'
      }, {
        'id': 'housekeeper',
        'title': 'Housekeeper',
        'subtitle': 'Manage successful analyses',
        'url': 'http://trailblazer.clinicalgenomics.se:8081/'
      }, {
        'id': 'clinstatsweb',
        'title': 'Clinstats Web',
        'subtitle': 'QC tools for post-alignment stats.',
        'url': 'http://trailblazer.clinicalgenomics.se:8083/'
      }, {
        'id': 'taboo',
        'title': 'Taboo',
        'subtitle': 'Genotype concordance testing',
        'url': 'http://trailblazer.clinicalgenomics.se:8080/'
      }, {
        'id': 'scout',
        'title': 'Scout',
        'subtitle': 'Variant visualizer and delivery portal',
        'url': 'http://scout.clinicalgenomics.se/'
      }, {
        'id': 'scout-beta',
        'title': 'Scout β',
        'subtitle': 'Variant visualizer (BETA)',
        'url': 'http://scout-demo.clinicalgenomics.se/'
      }, {
        'id': 'nipt',
        'title': 'NIPT Viewer',
        'subtitle': 'Visualize data from NIPT experiments',
        'url': 'https://clinical-db.scilifelab.se:8082/'
      }]
    }
  },
  components: {
    PageFooter,
    Tool
  }
}
</script>

<style>
  *, *:before, *:after {
    box-sizing: border-box;
  }

  html, body {
    height: 100%;
    padding: 0;
    margin: 0;
  }

  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    line-height: 1.5rem;
    font-size: 100%;
  }

  #app {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .section {
    padding: 2rem;
    overflow-y: auto;
  }

  .grid {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
  }

  .grid-item {
    margin-bottom: 5rem;
    flex-basis: 30%;

    display: flex;
    justify-content: center;
  }

  /* Small Devices, Tablets */
  @media (min-width: 768px) {
    .grid-item {
      flex-basis: 25%;
    }
  }

  /* Medium Devices */
  @media (min-width: 992px) {
    .grid-item {
      flex-basis: 20%;
    }
  }
</style>
