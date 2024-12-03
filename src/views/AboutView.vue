<script setup>
import imgSample from '@/assets/images/sample.png'
import imgDudu from '@/assets/images/dudu-cute.gif'
</script>

<template>
  <nav class="navbar bg-dark fixed-top" data-bs-theme="dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Sample App</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="offcanvas"
        data-bs-target="#offcanvasNavbar"
        aria-controls="offcanvasNavbar"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div
        class="offcanvas offcanvas-end"
        tabindex="-1"
        id="offcanvasNavbar"
        aria-labelledby="offcanvasNavbarLabel"
      >
        <div class="offcanvas-header">
          <h5 class="offcanvas-title" id="offcanvasNavbarLabel">Sample App</h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="offcanvas"
            aria-label="Close"
          ></button>
        </div>
        <div class="offcanvas-body">
          <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
            <li class="nav-item">
              <RouterLink class="nav-link active" aria-current="page" to="/">Login</RouterLink>
            </li>

            <li class="nav-item">
              <RouterLink class="nav-link" to="/register">Register</RouterLink>
            </li>

            <li class="nav-item">
              <RouterLink class="nav-link" to="/about">About</RouterLink>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </nav>

  <div class="container">
    <br /><br /><br />

    <div class="card">
      <div class="card-body text-center">
        <img :src="imgSample" width="50%" alt="" />

        <h1>About Us</h1>

        <hr />

        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione corporis officiis at
          facilis ea incidunt laborum quam. Tempore, veritatis. Sit saepe veniam fugit eius fugiat.
          Placeat quos expedita nostrum quis.
        </p>

        <hr />

        <p>
          <i>
            "Everybody should learn to program a computer because it teaches you how to think."
          </i>
          <br />
          <br />
          <u>- Steve Jobs -</u>
        </p>

        <img :src="imgDudu" width="50%" alt="" />
      </div>
    </div>

    <br /><br /><br /><br /><br />
  </div>

  <div class="fixed-bottom bg-dark border-top">
    <div class="container d-flex justify-content-around py-2">
      <!-- Login -->
      <RouterLink to="/" class="text-center text-decoration-none text-light">
        <i class="bi bi-box-arrow-in-right fs-4"></i>
        <div>Login</div>
      </RouterLink>

      <!-- Register -->
      <RouterLink to="/register" class="text-center text-decoration-none text-light">
        <i class="bi bi-person-plus fs-4"></i>
        <div>Register</div>
      </RouterLink>

      <!-- About -->
      <RouterLink to="/about" class="text-center text-decoration-none text-light">
        <i class="bi bi-question fs-4"></i>
        <div>About</div>
      </RouterLink>
    </div>
  </div>
</template>

<style scoped></style>
