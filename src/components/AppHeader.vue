<!-- JAVASCRIPT & VUE.JS -->
<script>
export default {
    data() {
        return {
            menuItems: [
                {
                    label: 'Home',
                    routeName: 'home',
                },
                {
                    label: 'Chi Siamo',
                    routeName: 'about-us',
                },
                {
                    label: 'Progetti',
                    routeName: 'projects-list',
                },
                {
                    label: 'Tipologie',
                    routeName: 'types-list',
                },
                {
                    label: 'Tecnologie',
                    routeName: 'technologies-list',
                },
                {
                    label: 'Contatti',
                    routeName: 'contacts',
                },
            ]
        }
    },
}
</script>

<!-- TEMPLATE HTML -->
<template lang="">
    <header>
        <nav class="navbar navbar-expand-lg bg-secondary py-3">
            <div class="container-fluid">
                <ul class="navbar-nav justify-content-center w-100">
                    <li class="nav-item" v-for="(item, index) in menuItems" :key="index">
                        <router-link :to="{ name: item.routeName }" v-text="item.label" class="nav-link text-white"></router-link>
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<!-- STYLE SCSS -->
<style lang="scss">
// IMPORTO GENERALS.SCSS
@use '../styles/generals.scss' as *;
</style>