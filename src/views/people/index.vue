<template>
  <div class="component">
    <div class="container--fluid">
      <h1>People</h1>
      {{ result }}
    </div>
  </div>
</template>

<script type="text/babel">
import PeopleService from '@/services/people'

export default {
  name: 'views-orders-index',
  watch: {},
  props: {},
  data() {
    return {
      result: undefined
    }
  },
  methods: {
    getPeople() {
      return PeopleService.getPeople()
          .then((result) => {
            this.result = result;
          })
    },
  },
  computed: {},
  created() {
  },
  mounted() {
    this.getPeople();
  },
  beforeDestroy() {
  },
  mixins: [],
  components: {}
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
