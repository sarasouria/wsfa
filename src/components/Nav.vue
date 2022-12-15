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
      <i class="fas fa-bars"></i>
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