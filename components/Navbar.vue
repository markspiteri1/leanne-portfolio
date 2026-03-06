<template>
    <nav>
        <h1 class="text-3xl md:text-5xl font-medium cursor-pointer" @click="$router.push('/')">Leanne Lewis</h1>
            <div id="nav-icon3" class="navbar" :class="{ open: isMenuOpen }" @click="toggleOpen">
                <div class="h-20">
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>

            <!-- Overlay Menu -->
            <div class="menu-overlay" :class="{ active: isMenuOpen }" @click="toggleOpen">
                <div class="menu-content" @click.stop>
                    <a class="navbar-item" href="/" @click="toggleOpen">Home</a>
                    <a class="navbar-item" href="/about" @click="toggleOpen">About</a>
                    <a class="navbar-item" href="/work" @click="toggleOpen">Work</a>
                </div>
            </div>
    </nav>
</template>
<script setup>
const isMenuOpen = ref(false);
const toggleOpen = () => {
    isMenuOpen.value = !isMenuOpen.value;
};
</script>
<style>
/* Icon 3 */
#nav-icon3 span:nth-child(1) {
    top: 0px;
}

#nav-icon3 span:nth-child(2),
#nav-icon3 span:nth-child(3) {
    top: 12px;
}

#nav-icon3 span:nth-child(4) {
    top: 24px;
}

#nav-icon3.open span:nth-child(1) {
    top: 12px;
    width: 0%;
    left: 50%;
}

#nav-icon3.open span:nth-child(2) {
    -webkit-transform: rotate(45deg);
    -moz-transform: rotate(45deg);
    -o-transform: rotate(45deg);
    transform: rotate(45deg);
}

#nav-icon3.open span:nth-child(3) {
    -webkit-transform: rotate(-45deg);
    -moz-transform: rotate(-45deg);
    -o-transform: rotate(-45deg);
    transform: rotate(-45deg);
}

#nav-icon3.open span:nth-child(4) {
    top: 12px;
    width: 0%;
    left: 50%;
}

/* Overlay Menu Styles */
.menu-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.95);
    z-index: 1000;
    opacity: 0;
    visibility: hidden;
    transition: opacity 0.3s ease, visibility 0.3s ease;
    display: flex;
    align-items: center;
    justify-content: center;
}

.menu-overlay.active {
    opacity: 1;
    visibility: visible;
}

.menu-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
}

.navbar-item {
    color: white;
    font-size: 2rem;
    font-weight: 300;
    text-decoration: none;
    transition: all 0.2s ease;
    padding: 1rem 2rem;
    border-radius: 8px;
    position: relative;
    overflow: hidden;
}

.navbar-item:hover {
    color: rgba(255, 255, 255, 0.7);
    transform: scale(1.02);
}

.navbar-item::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(255, 255, 255, 0.03);
    opacity: 0;
    transition: opacity 0.2s ease;
    z-index: -1;
}

/* Update navbar icon positioning */
#nav-icon3 {
    position: fixed;
    top: 2rem;
    right: 2rem;
    z-index: 1001;
    width: 40px;
    height: 35px;
    -webkit-transform: rotate(0deg);
    -moz-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
    -webkit-transition: .5s ease-in-out;
    -moz-transition: .5s ease-in-out;
    -o-transition: .5s ease-in-out;
    transition: .5s ease-in-out;
    cursor: pointer;
}

#nav-icon3 span {
    display: block;
    position: absolute;
    height: 2px;
    width: 100%;
    background: #424242;
    opacity: 1;
    left: 0;
    -webkit-transform: rotate(0deg);
    -moz-transform: rotate(0deg);
    -o-transform: rotate(0deg);
    transform: rotate(0deg);
    -webkit-transition: .25s ease-in-out;
    -moz-transition: .25s ease-in-out;
    -o-transition: .25s ease-in-out;
    transition: .25s ease-in-out;
}
</style>