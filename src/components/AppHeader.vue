<script>
export default {
    data() {
        return {
            activeIndex: false,
            menu: [
                {
                    title: "home",
                    routeName: "home",
                },
                {
                    title: "About",
                    routeName: "about",
                },
            ]
        }
    }

}
</script>
<template>
    
        <nav class="navbar navbar-expand-lg bg-dark">
            <div class="container">
                <a class="navbar-brand text-light" href="#">BoolFolio</a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav gap-3">
                        <li class="nav-item" v-for="curLink in menu">
                            <router-link :class="[activeIndex = true]" :to="{ name: curLink.routeName }">
                                {{ curLink.title }}
                            </router-link>
                        </li>
                    </ul>   
                </div>
            </div>
        </nav>

   

</template>