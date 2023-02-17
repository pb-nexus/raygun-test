<template>
  <div>
    <button @click="hello">Hello</button>
    <button @click="error">Error</button>
  </div>
</template>

<script setup lang="ts">


// ->> AppSignal--------------------------------------

// import Appsignal from "@appsignal/javascript"

// const appsignal = new Appsignal({ 
//   key: "02b07710-172c-4779-91bf-a05ac8f633e4",
//   namespace: "nuxt",
// })



// ->> TrackJS--------------------------------------

  // import { TrackJS } from 'trackjs';
  // TrackJS.install({
  //   token: "77f5555336e34b6c993af45618d5373c",
  //   application: "pb-test"
  //   // for more configuration options, see https://docs.trackjs.com
  // });



// ->> SENTRY--------------------------------------

// import * as Sentry from "@sentry/browser";
// import { BrowserTracing } from "@sentry/tracing";

// Sentry.init({
//   dsn: "https://61977d9ea2b7492b97c8fe2f8d6fa30b@o4504690427559936.ingest.sentry.io/4504690444795904",
//   integrations: [new BrowserTracing()],
//   tracesSampleRate: 1.0,
// });



// ->> RAYGUN -------------------------------------

// const config = useRuntimeConfig();

// const key = config.public.raygunApiKey

// useHead({
//   script: [
//     {
//       hid: 'Ruygun init',
//       innerHTML: `!function(a,b,c,d,e,f,g,h){a.RaygunObject=e,a[e]=a[e]||function(){(a[e].o=a[e].o||[]).push(arguments)},f=b.createElement(c),g=b.getElementsByTagName(c)[0],f.async=1,f.src=d,g.parentNode.insertBefore(f,g),h=a.onerror,a.onerror=function(b,c,d,f,g){h&&h(b,c,d,f,g),g||(g=new Error(b)),a[e].q=a[e].q||[],a[e].q.push({e:g})}}(window,document,"script","//cdn.raygun.io/raygun4js/raygun.min.js","rg4js");`,
//       type: "text/javascript",
//     },
//     {
//       hid: 'Ruygun config',
//       innerHTML: `rg4js('apiKey','${key}');rg4js('enableCrashReporting', true);rg4js('enablePulse', true);`,
//       type: "text/javascript",
//     }
//   ]
// })


function hello(){
  console.log('Hello')
}
function error(){
  console.log(undefined()()()());
}
</script>