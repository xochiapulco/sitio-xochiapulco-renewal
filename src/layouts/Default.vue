<template>
    <div class="layout">
        <Header></Header>

        <header class="header">
            <strong>
                <g-link to="/">{{ $static.metadata.siteName }}</g-link>
            </strong>
            <nav class="nav">
                <g-link class="nav__link" to="/">Home</g-link>
                <g-link class="nav__link" to="/about/">About</g-link>
            </nav>
        </header>
        <slot />
    </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import Header from '~/components/Header';

export default {
    components: { Header },
};
</script>

<style></style>
