<template>
  <div>
    <p class="mb-10" v-for="(paragraph, index) in displayText" v-bind:key="index">
      {{ paragraph }}
    </p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    props: {
        paragraphs: {
            type: Number,
            default: 5
        }
    },
    data () {
      return {
          rawText: null
      }
    },
    computed: {
        displayText () {
            return this.rawText || []
        }
    },
    async mounted() {
        const { data: text } = await axios.get(`https://baconipsum.com/api/?type=meat-and-filler&paras=${this.paragraphs}&format=json`)
        this.rawText = text
    }

}
</script>

<style>

</style>