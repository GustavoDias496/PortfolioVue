<script>
export default {
    data() {
        return {
            showMobileMenu: false,
        };
    },
    methods: {
        showMenu() {
            this.showMobileMenu = !this.showMobileMenu;
        },
    },
};
</script>

<template>
    <div>
        <div class="nav-menu">
            <img class="menuIcon" @click="showMenu()" src="../assets/menu.svg" alt="" height="30px" width="30px">
            <div class="nav-content" :class="this.showMobileMenu ? 'open-menu' : 'closed-menu'">

                <ul class="nav-items">
                    <li><a href="#">Início</a></li>
                    <li><a href="#projects">Projetos</a></li>
                    <li><a href="#skills">Habilidades</a></li>
                </ul>
                <div class="login-button">Login</div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.nav-menu {
    background-color: var(--color-background);
    border-bottom: 3px solid var(--color-margin);
    position: fixed;
    /* Adicionado */
    top: 0;
    /* Adicionado */
    width: 100%;
    /* Adicionado */
}

.nav-content {
    display: flex;
    justify-content: center;
    align-items: center;
}

.nav-items {
    list-style: none;
    display: flex;
    margin-right: 30px;
}

ul li a {
    font-weight: 400;
    margin-right: 10px;
    text-decoration: none;
    color: var(--color-text-primary);
}

ul li a:hover {
    color: var(--color-text-secondary);
    cursor: pointer;
}

.logo img {
    width: 30px;
    height: 30px;
}

img {
    display: none;
}

@media screen and (max-width: 900px) {
    .nav-menu {
        padding-top: 10px;
        position: absolute;
        width: 100%;
        position: fixed;
        top: 0;
    }

    .open-menu {
        opacity: 1;
        height: 100px;
    }

    .closed-menu {
        opacity: 0;
        height: 0;
        padding: 0;
    }

    .nav-content {
        display: flex;
        flex-direction: column;
        z-index: 100;
        position: relative;
        transition: all 0.2s ease-out;
        align-items: center;
        justify-content: center;
    }

    .nav-items {
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    .nav-items li {
        margin-bottom: 10px;
    }

    img {
        display: block;
        text-align: right;
        padding: 0 10px 10px 0;
    }
}
</style>