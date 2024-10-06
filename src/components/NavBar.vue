<template>
    <div id="navigation" class="montserrat">
        <router-link :to="{ name: 'home' }" id="home">
            <img src="@/assets/cherry2.png" alt="Cherry icon" id="cherry">
        </router-link>
        <router-link :to="{ name: 'timeline' }">
            <p>Timeline</p>
        </router-link>
        <router-link :to="{ name: 'songs' }">
            <p>Songs</p>
        </router-link>
        <router-link :to="{ name: 'letter' }">
            <p>Letter</p>
        </router-link>
    </div>
</template>

<script>
</script>

<style scoped>
#navigation {
    background-color: #fae1dd;
    height: 4rem;
    display: flex;
    justify-content: center;
    align-items: center;
    column-gap: 2rem;
    width: 100%;
}

a {
    text-decoration: none;
    color: #f5b2b7;
}

p{
    font-size: 16px;
}

#cherry{
    width: 3em;
}

#home{
    flex-basis: 6em;
}
</style>