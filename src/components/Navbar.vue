<template>
    <nav 
        :class="[`navbar-${theme}`, `bg-${theme}`, 'navbar', 'navbar-expand-lg']">
        <a class="navbar-brand" href="#">Vue Project</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarText">
          <ul class="navbar-nav mr-auto">
            <li v-for="(page, index) in pages" class="nav-item" :key="index">
                <a
                    class="nav-link "
                    :class="{ active: activePage == index }"
                    aria-current="page"
                    :href="page.link.url"
                    :title="`This Link Goes To ${page.text}`"
                    @click.prevent="navLinkClick(index)"
                    >{{ page.link.text }}</a>
              </li>
          </ul>
          <form class="d-flex">
            <button class="btn btn-primary"
            @click.prevent="changeTheme()"
            >Toggle
            </button>
          </form>
        </div>
      </nav>
</template>

<script>
    export default{
        props: ['pages', 'activePage', 'navLinkClick'],
        data() {
            return{
                theme: 'light',
            }

        },
        methods: {
                    changeTheme() {
                        this.theme = this.theme === 'light' ? 'dark' : 'light';
                        }
                }

    }

</script>



<style>

</style>