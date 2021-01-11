<template>
  <p>Reaction Time: {{ score }} ms</p>
  <p class="rank">You got {{ rank }} rank</p>
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
        switch (true) {
            case this.score < 150:
                this.rank = "S";
                break;
            case this.score < 200:
                this.rank = "A";
                break;
            case this.score < 250:
                this.rank = "B";
                break;
            case this.score < 300:
                this.rank = "C";
                break;
            case this.score < 350:
                this.rank = "D";
                break;
            case this.score < 400:
                this.rank = "F";
                break;
            default:
                this.rank = "No"
                break;
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
    
</style>