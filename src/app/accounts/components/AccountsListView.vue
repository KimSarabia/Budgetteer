<template>
  <div id="accounts-list-view">
    I'm a list of accounts!
    
    <router-link :to="{ name: 'createEditAccount' }">Add an account</router-link>
    
    <ul>
      <li v-for="account, key in accounts">
        {{ account.name }}
        <span class="tag is-small is-info">{{ categories[account.category] }}</span>
        ${{ account.balance }}
      </li>
    </ul>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'accounts-list-view'
}
</script>

<style scoped lang='scss'>
#accounts-list-view {
}
</style>