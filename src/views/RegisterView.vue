<script setup>
import imgSample from '@/assets/images/sample.png'
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

    <div class="row">
      <div class="col-sm-12 text-center">
        <img :src="imgSample" width="50%" alt="" />
        <h1 class="fw-bold">Sample App</h1>
        <h2>Registration</h2>
      </div>
      <div class="col-sm-12">
        <hr />
        <div class="card">
          <div class="card-body">
            <!-- Register Form -->
            <form class="form-floating">
              <div class="form-floating mb-3">
                <input type="text" class="form-control" placeholder="Firstname" required />
                <label>Firstname</label>
              </div>

              <div class="form-floating mb-3">
                <input type="text" class="form-control" placeholder="Lastname" required />
                <label>Lastname</label>
              </div>

              <div class="form-floating mb-3">
                <input type="email" class="form-control" placeholder="name@example.com" required />
                <label>Email address</label>
              </div>

              <div class="form-floating mb-3">
                <input type="password" class="form-control" placeholder="Password" required />
                <label>Password</label>
              </div>

              <div class="form-floating mb-3">
                <input
                  type="password"
                  class="form-control"
                  placeholder="Confirm Password"
                  required
                />
                <label>Confirm Password</label>
              </div>

              <button type="submit" class="btn btn-primary w-100 fw-bold">
                <i class="bi bi-person-add"></i>
                Register
              </button>
            </form>
          </div>
        </div>

        <hr />

        <div class="text-center">
          Already have account? <RouterLink to="/"><b>Login Here</b></RouterLink>
        </div>
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
