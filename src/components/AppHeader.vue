<script>
export default {
    data() {
        return {
            activeIndex:false,
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
    <nav>
        <ul class="d-flex gap-5" >
            <li v-for="curLink in menu">
                <router-link
                :class="[activeIndex=true]"
                :to="{name:curLink.routeName}">
                    {{ curLink.title }}
                </router-link>
            </li>
        </ul>
    </nav>
</template>