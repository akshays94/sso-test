<template>
<div>
    <button @click="navigate()">Login SSO</button>
    <router-link :to="{ name: 'Home' }">Home</router-link>
</div>
</template>

<script>
export default {
    created () {
        let query = this.$route.query
        console.log(query)
        if (query) {
            if ('isAuthenticated' in query) {
                this.$router.push(this.$route.path)
                alert(`Authenticated: ${query.email}`)
                console.log('query', query)
            } 
        }
    },
    methods: {
        navigate () {
            // let url = 'https://rhombusdevteam-dev.onelogin.com/trust/saml2/http-post/sso/398e7049-05d0-4966-a3f9-23bbd542b665'
            let url = 'https://rhombusdevteam-dev.onelogin.com/trust/saml2/http-redirect/sso/09c00e96-cdec-4319-ab46-941b6d324ede'
            window.location.href = url
        }
    }
}
</script>