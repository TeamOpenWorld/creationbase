<template>
    <div>
        <nav
            class="navbar header has-shadow is-primary"
            role="navigation"
            aria-label="main navigation"
        >
            <div class="navbar-brand">
                <a class="navbar-item" href="/">
                    <h1>Creationbase (beta)</h1>
                </a>

                <div class="navbar-burger">
                    <span />
                    <span />
                    <span />
                </div>
            </div>
        </nav>

        <section class="main-content columns">
            <aside class="column is-2 section">
                <p class="menu-label is-hidden-touch">
                    Menu
                </p>
                <ul class="menu-list">
                    <li v-for="(item, key) of items" :key="key">
                        <nuxt-link :to="item.to" exact-active-class="is-active">
                            <b-icon :icon="item.icon" /> {{ item.title }}
                        </nuxt-link>
                    </li>
                </ul>
            </aside>

            <div class="container column is-10">
                <nuxt />
            </div>
        </section>

        <footer class="footer">
            <div class="content has-text-centered">
                <p>
                    <strong>Creationbase</strong> by
                    <a href="https://jgthms.com">Minato Minami</a>. This website
                    licensed <a href="">MPL-2.0</a>. The website content and
                    database is licensed
                    <a
                        href="https://creativecommons.org/licenses/by/4.0/deed.ja"
                        target="_blank"
                        >CC BY 4.0</a
                    >.
                </p>
            </div>
        </footer>
    </div>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    title: "Top",
                    icon: "home",
                    to: { name: "index" }
                },
                {
                    title: "Search",
                    icon: "magnify",
                    to: { name: "search" }
                },
                {
                    title: "History",
                    icon: "history",
                    to: { name: "inspire" }
                }
            ]
        };
    }
};
</script>
