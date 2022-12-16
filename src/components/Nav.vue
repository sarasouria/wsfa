<template>
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <button
      class="navbar-toggler"
      type="button"
      data-mdb-toggle="collapse"
      data-mdb-target="#navbarTogglerDemo03"
      aria-controls="navbarTogglerDemo03"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" class="bi bi-list" viewBox="0 0 16 16">
        <path fill-rule="evenodd" d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zm0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5z"/>
      </svg>
    </button>
    <RouterLink to="/" class="navbar-brand">Wasfa</RouterLink>
    <div class="collapse navbar-collapse" id="navbarTogglerDemo03">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">       
        <li class="nav-item active">
            <RouterLink to="/" class="nav-link">Home</RouterLink>
        </li>
        <li class="nav-item">
            <RouterLink to="/about" class="nav-link">About</RouterLink>
        </li>
      </ul>
      <form class="d-flex input-group w-auto" v-on:submit.prevent="search">
        <input
          type="search"
          class="form-control"
          placeholder="Looking for a meal ..."
          aria-label="Search"
          v-model="searchForm.query"
        />
        <input
          class="btn btn-outline-primary"
          type="submit"
          data-mdb-ripple-color="dark"
          value="Search"
        />
      </form>
    </div>
  </div>
</nav>
</template>
<script>
    export default{
    data()
    {
        return{
            searchForm:{
                query:''
            }
        }
    },
    methods:{
        search()
        {
            this.$router.push({ name: 'result', params: { query: this.searchForm.query }});   
           // this.$router.go(0);    
        }
    }
    }
    
</script>