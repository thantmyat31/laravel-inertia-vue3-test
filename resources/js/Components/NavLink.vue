<template>
    <Link 
        href="/"
        class="text-decoration-none"
        :class="{'fw-bold text-decoration-underline': active}"
    >
        <slot />
    </Link>
</template>

<script>
import { Link } from '@inertiajs/inertia-vue3';

export default {
    props: {
        active: Boolean,
        name: String
    },
    components: {
        Link
    },
};
</script>