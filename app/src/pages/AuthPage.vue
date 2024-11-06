<script >
import { defineComponent, onMounted, onUnmounted } from 'vue';
export default defineComponent({
    setup() {
        const loadScript = (src) => {
            const script = document.createElement('script');
            script.type = 'text/javascript';
            script.src = src;
            script.id = 'supertokens-script';
            script.onload = () => {
                (window).supertokensUIInit("supertokensui", {
                    appInfo: {
                        appName: "Nuggets",
                        apiDomain: "https://localhost:5000",
                        websiteDomain: "https://localhost:9000/#",
                        apiBasePath: "/auth",
                        websiteBasePath: "/auth"
                    },
                    recipeList: [
                        (window).supertokensUIEmailPassword.init(),
                        (window).supertokensUIThirdParty.init({
                            signInAndUpFeature: {
                                providers: [
                                    (window).supertokensUIThirdParty.Github.init(),
                                    (window).supertokensUIThirdParty.Google.init(),
                                    (window).supertokensUIThirdParty.Facebook.init(),
                                    (window).supertokensUIThirdParty.Apple.init(),
                                ]
                            }
                        }),
                        (window).supertokensUISession.init(),
                    ],
                });
            };
            document.body.appendChild(script);
        };

        onMounted(() => {
            loadScript('https://cdn.jsdelivr.net/gh/supertokens/prebuiltui@v0.47.0/build/static/js/main.00ec3e91.js');
        });

        onUnmounted(() => {
            const script = document.getElementById('supertokens-script');
            if (script) {
                script.remove();
            }
        });
    },
});
</script>

<template>
    <div id="supertokensui" />
</template>