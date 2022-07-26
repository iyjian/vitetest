<script setup>
import { ref } from 'vue'

defineProps({
  msg: String
})

const count = ref(0)
</script>

<template>
<span>fuck</span>
</template>
<script>
import * as Minio from 'minio'
// import fxp from "fast-xml-parser"
// import * as Minio from '/Users/wuchong/projects/forked/minio-js/dist/main/minio.js'
// const Minio = require('/Users/wuchong/projects/forked/minio-js/dist/main/minio.js')

export default {
  name: 'Login',
  mounted () {
    const c = new Minio.Client({
      accessKey: 'RhRkAQYN5cDsdvZK',
      secretKey: 'TEYZqZDMLd3zIWIIun7IDhy7FtKapuhw',
      endPoint: '0.0.0.0',
      port: 9000,
      useSSL: false
    })
    c.listBuckets().then(console.log)
  }
}
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
