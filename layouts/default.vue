<template>
  <div>

    <header class="container">
      <Header></Header>
    </header>

    <menu class="container">
      <Menu></Menu>
    </menu>

    <section class="container flex">
      <main class="main">
        <nuxt />
      </main>
      <aside class="sidebar">
        <Sidebar></Sidebar>
      </aside>
    </section>

    <footer class="container">
      <Footer></Footer>
    </footer>

  </div>
</template>

<script>

import Header from "@/components/layout/Header"
import Footer from "@/components/layout/Footer"
import Sidebar from "@/components/layout/Sidebar"
import Menu from "@/components/layout/Menu"

export default {
  components: {
    Header, Footer, Sidebar, Menu
  }
}
</script>