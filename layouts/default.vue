<template>
  <div>
    <Header />
    <div class="shadow" />
    <div id="main" class="container" role="main">
      <div class="grid">
        <div id="column__main" class="grid__item">
          <div class="inner">
            <Nuxt />
          </div>
        </div>
        <div id="column__sidebar" class="grid__item">
          <div class="inner">
            <Sidebar />
          </div>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script></script>

<style></style>
