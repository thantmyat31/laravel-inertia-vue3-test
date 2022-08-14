<template>
    <nav class="my-2 col">
        <ul class="row align-items-center">
            <li class="col">
                <NavLink href="/" :active="$page.component === 'Home'">
                    Home
                </NavLink>
            </li>
            <li class="col">
                <NavLink href="/users" :active="$page.component === 'Users'">
                    Users
                </NavLink>
            </li>
            <li class="col">
                <NavLink href="/settings" :active="$page.component === 'Settings'">
                    Settings
                </NavLink>
            </li>
            <li class="col">
                <Link 
                    href="/logout"
                    class="text-decoration-none"
                    method="post" :data="{foo: 'bar'}" as="button">Logout</Link>
            </li>
        </ul>
    </nav>
</template>

<script>
import {Link} from '@inertiajs/inertia-vue3';
import NavLink from './NavLink';

export default {
    components: {
        Link,
        NavLink
    }
};
</script>