<template>
  <header class="container">
    <div class="grid grid--rev">
      <div id="header__left" class="grid__item">
        <h1 class="logo">
          <nuxt-link to="/">
            <Logo />
          </nuxt-link>
        </h1>
      </div>
      <div id="header__right" class="grid__item">
        <div class="inner">
          <div class="tagline">
            <p>Higher Education <strong>Solved</strong>.</p>
          </div>
          <nav>
            <ul class="nav">
              <li id="nav-home" class="nav-item">
                <nuxt-link to="/">Home</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link to="/services">Services</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link to="/clients">Clients</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link to="/partners">Partners</nuxt-link>
              </li>
              <li class="nav-item">
                <nuxt-link to="/about">About</nuxt-link>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup></script>

<style lang="scss" scoped></style>
