<script setup>

</script>

<template>
  <header>
    <div id="sidebar" class="d-flex flex-column flex-shrink-0 p-3 text-white bg-dark" style="width: 220px;">
      <a href="/" class="d-flex  align-items-center mb-3 mb-md-0 me-md-auto text-white text-decoration-none">
        <!-- <svg class="bi me-2" width="40" height="32">
          <use xlink:href="#bootstrap"></use>
        </svg> -->
        <span class="fs-7">Myport.Pro Admin</span>
      </a>
      <hr>
      <ul class="nav nav-pills flex-column mb-auto">
         <li>
          <router-link
            to="/"
            custom
            v-slot="{ href, navigate}"
          >
            <a :href="href" class="nav-link text-white" @click="navigate">
              <font-awesome-icon width="16" height="16" class="me-2" icon="fa-solid fa-house" />
              Home
            </a>
          </router-link>
        </li>
        <li>
          <router-link
            to="/account"
            custom
            v-slot="{ href, navigate}"
          >
            <a :href="href" class="nav-link text-white" @click="navigate">
              <font-awesome-icon width="16" height="16" class="me-2" icon="fa-solid fa-user" />
              Account
            </a>
          </router-link>
        </li>
        <li>
          <router-link
            to="/pair"
            custom
            v-slot="{ href, navigate}"
          >
          <a :href="href" class="nav-link text-white " @click="navigate">
            <font-awesome-icon width="16" height="16" class="me-2" icon="fa-solid fa-dollar-sign" />
            Pair
          </a>
          </router-link>
        </li>
        <li>
           <router-link
            to="/strategy"
            custom
            v-slot="{ href, navigate}"
          >
          <a :href="href" class="nav-link text-white" @click="navigate">
            <font-awesome-icon width="16" height="16" class="me-2" icon="fa-solid fa-circle-info" />
            Strategy
          </a>
          </router-link>
        </li>
      </ul>
      <hr>
      <div class="dropdown">
        <a href="#" class="d-flex align-items-center text-white text-decoration-none dropdown-toggle" id="dropdownUser1"
          data-bs-toggle="dropdown" aria-expanded="false">
          <img src="" alt="" width="32" height="32" class="rounded-circle me-2">
          <strong>John Doe</strong>
        </a>
        <ul class="dropdown-menu dropdown-menu-dark text-small shadow" aria-labelledby="dropdownUser1">
          <li><a class="dropdown-item" href="#">New project...</a></li>
          <li><a class="dropdown-item" href="#">Settings</a></li>
          <li><a class="dropdown-item" href="#">Profile</a></li>
          <li>
            <hr class="dropdown-divider">
          </li>
          <li><a class="dropdown-item" href="#">Sign out</a></li>
        </ul>
      </div>
    </div>
  </header>

  <main>
    <RouterView />
  </main>

</template>

<style scoped>
#sidebar {
  height: 100%;
  position: fixed;
}

main {
  margin-left: 220px;
}
</style>
