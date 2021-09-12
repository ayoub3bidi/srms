<template>
  <div>
    <!-- Nav bar -->
    <nav class="navbar navbar-expand-md bg-dark navbar-dark">
      <!-- Brand -->
      <a style="padding-left: 10px" class="navbar-brand" href="#">S.R.M.S</a>

      <!-- Toggler/collapsibe Button -->
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#collapsibleNavbar">
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Navbar links -->
      <div class="collapse navbar-collapse" id="collapsibleNavbar">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link pr-3" to="/">Create Student</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/view">View Students</router-link>
          </li>
        </ul>
      </div>
    </nav>
    <!-- Router view -->
    <div class="container mt-5">
      <router-view></router-view>
    </div>
    <!-- footer -->
    <footer class="py-5">
      <div class="container">
        <div class=" text-center text-muted">Copyright © 2021 | Ayoub Abidi
        </div>
      </div>
    </footer>
  </div>
</template>