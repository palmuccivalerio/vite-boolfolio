<script>
export default {
    data() {
        return {};
    },
};
</script>

<template>
    <nav
        class="navbar navbar-expand-lg bg-dark border-bottom border-body py-3"
        data-bs-theme="dark"
    >
        <div class="container-fluid">
        <a class="navbar-brand" href="#">Boolfolio</a>
        <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
        >
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
            <li class="nav-item">
                <router-link :to="{ name: 'home' }" class="nav-link">
                    Home
                </router-link>
            </li>
            <li class="nav-item">
                <router-link :to="{ name: 'projects' }" class="nav-link">
                    Projects
                </router-link>
            </li>
            </ul>
        </div>
        </div>
    </nav>
</template>

<style scoped lang="scss"></style>