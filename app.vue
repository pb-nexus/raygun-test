<template>
  <div>
    <button @click="hello">Hello</button>
    <button @click="error">Error</button>
  </div>
</template>

<script setup lang="ts">
const config = useRuntimeConfig();

const key = config.public.raygunApiKey

useHead({
  script: [
    {
      hid: 'Ruygun init',
      innerHTML: `!function(a,b,c,d,e,f,g,h){a.RaygunObject=e,a[e]=a[e]||function(){(a[e].o=a[e].o||[]).push(arguments)},f=b.createElement(c),g=b.getElementsByTagName(c)[0],f.async=1,f.src=d,g.parentNode.insertBefore(f,g),h=a.onerror,a.onerror=function(b,c,d,f,g){h&&h(b,c,d,f,g),g||(g=new Error(b)),a[e].q=a[e].q||[],a[e].q.push({e:g})}}(window,document,"script","//cdn.raygun.io/raygun4js/raygun.min.js","rg4js");`,
      type: "text/javascript",
    },
    {
      hid: 'Ruygun config',
      innerHTML: `rg4js('apiKey','${key}');rg4js('enableCrashReporting', true);rg4js('enablePulse', true);`,
      type: "text/javascript",
    }
  ]
})

function hello(){
  console.log('Hello')
}
function error(){
  console.log(undefined()()()());
}
</script>