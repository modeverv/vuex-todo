<template>
<div>
  Formページ
  <head-comp></head-comp>
  <textarea-comp></textarea-comp>
  <string-comp></string-comp>
  <button @click="buttonAction">{{button}}</button>
</div>
</template>

<script>

import HeadComp from '@/components/modules/HeadComp'
import TextareaComp from '@/components/modules/TextareaComp'
import StringComp from '@/components/modules/StringComp'
import { mapActions, mapGetters } from 'vuex'

export default {
  name: 'Form',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
    }
  },
  computed: mapGetters('Form', {
    'button': 'getButton'
  }),
  methods: mapActions('From',{
    'buttonAction' : 'buttonAction'
  }),
  components: {
    HeadComp,
    TextareaComp,
    StringComp
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
