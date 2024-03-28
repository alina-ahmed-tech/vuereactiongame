  <template>
     <p>Reaction Time: {{ score }} ms</p>
     <p class="rank">{{ rank }}</p>
  </template>
  
  <script>
  export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'OMG Super Fast!'
        } else if (this.score < 400) {
            this.rank = 'Quite Speedy'
        } else {
            this.rank = 'Are you a human or are you a snail...'
        }
    }
  }
  </script>
  
  <style>
    .rank {
        font-size: 1.4em;
        color:blueviolet;
        font-weight: bold;
    }
  </style>