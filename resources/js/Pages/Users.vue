<template>
    <Layout>
        <Nav />
        <h1>Users</h1>

        <div class="py-5" style="margin-top:500px">
            <p>This current time is {{ time }}.</p>
            <Link 
                href="/users"
                preserve-scroll
            >
                Refresh
            </Link>
        </div>
    </Layout>
</template>

<script>
import Layout from '../Components/Layout.vue';
import {Link} from '@inertiajs/inertia-vue3';

export default {
    components: {
    Link,
    Layout
},
    props: {
        time: String
    }
};
</script>