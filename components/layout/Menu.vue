<template>
    <nav class="menu flex">
        <nuxt-link class="menu__link" to="/">Portada</nuxt-link>
        <nuxt-link class="menu__link" to="/tiempos/lista">Tiempos</nuxt-link>
        <nuxt-link class="menu__link" to="/historia">Historia</nuxt-link>
        <nuxt-link class="menu__link" to="/contacto">Contacto</nuxt-link>
    </nav>
</template>

<style lang="scss">
    
    // Metodologia BEM de CSS
    .menu {

        background-color: #333;

        &__link {
            color: #eee;
            text-decoration: none;
            padding: 1rem;

            &:hover {
                background-color: #000;
            }
        }

    }

</style>