<template>
<h1>{{title}}</h1>  
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: "headComp",
  data() {
    return {
      title: "感想を入力"
    };
  },
  computed: mapGetters({'title': 'getTitle'})
};
</script>
