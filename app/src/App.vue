<template>
  <router-view />
</template>

<script setup>

import SuperTokens from "supertokens-web-js";
import Session from "supertokens-web-js/recipe/session";

SuperTokens.init({
    appInfo: {
      appName: "Nuggets",
      apiDomain: "https://localhost:5000",
      websiteDomain: "https://localhost:9000",
      apiBasePath: "/auth",
      websiteBasePath: "/auth"
    },
    recipeList: [
        Session.init(),
    ],
});


defineOptions({
  name: 'App'
});


</script>
