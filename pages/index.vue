<template>
  <div>
    <h1>전원식이 넉스트를 통하여 홈피를 만들고 있습니다.</h1>
    <nuxt-link to="search">검색페이지로 이동</nuxt-link>
    <form 
      @submit.prevent = "search()">
      <input type="text" v-model="jtext"><button>검색</button>
    </form>
  </div>
</template>

<script>
export default {
  data :()=> {
    return {jtext:'',}
  },
  methods: {
    search() {
        if(this.jtext.length <2) return alert('두글자 이상 작성해야합니다.')
        this.$router.push('/search')
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
