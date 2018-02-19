```js
<script>
import vWizard from 'vue-wizard'

export default {
  components: {
    vWizard
  },
  computed: {
    ...mapGetters({
      route: types.GET_ROUTE,
      steps: types.GET_STEPS
    }),
    step: {
      get() {
        return this.route
      },
      set(route) {
        this.$commit('COMMIT_STEP', route)
      }
    }
  }
}
</script>
```