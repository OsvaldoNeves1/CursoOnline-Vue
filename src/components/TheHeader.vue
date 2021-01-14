<template>
    <header>
        <nav>
            <div class="logo">
                <router-link to="/">Escola de Tecnologia</router-link>
            </div>
            <ul>
                <li>
                    <router-link to="/cursos">Cursos</router-link>
                </li>
                <li>
                    <router-link to="/contato">Contato</router-link>
                </li>
            </ul>
        </nav>
    </header>
</template>


<script>
export default {
    name:"TheHeader"
}
</script>


<style scoped>

header {
    background:#09005d;
}

header a {
    color: #fff;
}

a.router-link-exact-active {
  color:#f6716a;
}

nav {
    max-width: 950px;
    margin: 0 auto;
    display: flex;
    align-content: space-between;
    padding: 20px;
}

.logo {
    flex:1
}

.logo a {
    font-family: 'Source Sans Pro', sans-serif;
    font-weight: lighter;
    font-size: 1.5rem;
    color: #fff;
}

ul li {
    display: inline-block;
}

li a {
    font-family: 'Source Sans Pro', sans-serif;
    font-weight: lighter;
    font-size: 1.3rem;
    padding: 0 10px;
    margin-left: 15px;
}

</style>