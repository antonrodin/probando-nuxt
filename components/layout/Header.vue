<template>
    <div class="header flex items-center">
        <nuxt-link to="/">
            <img class="header__logo" src="/logo.png" alt="Logotipo">
        </nuxt-link>

        <div class="header__desc">
            <h1>Circuito de Nürburgring</h1>
            <p>Pagina no oficial sobre Nürburgring. Todo tipo de información útil sobre este legendario circuito, considerado como una "Meca" para muchos amantes del mundo del motor.</p>
        </div>
    </div>
</template>

<style lang="scss">
    .header {
        &__logo {
            margin: 1rem;
            margin-right: 6rem;
        }
    }
</style>