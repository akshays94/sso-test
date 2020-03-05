<template>
<div>
    <button @click="navigate()">Login SSO</button>
</div>
</template>

<script>
export default {
    created () {
    },
    methods: {
        navigate () {
            let url = 'https://rhombusdevteam-dev.onelogin.com/trust/saml2/http-post/sso/398e7049-05d0-4966-a3f9-23bbd542b665'
            window.location.href = url
        }
    }
}
</script>