<template>
    <header class="bg-info">
        <div class="container">
            <div class="row align-items-center">
                <div class="col">
                    <h2>My App</h2>
                    <p>Welcome Back, {{ username }}</p>
                </div>
                <Nav />
            </div>
        </div>
    </header>
    <div class="container">
        <slot />
    </div>
</template>

<script>
import Nav from './Nav';
export default {
    components: {
        Nav
    },
    computed: {
        username() {
            return this.$page.props.auth.user.username;
        }
    }
};
</script>