# Navigation

Nuxt automatically creates a cue-router configeration based on the files in the
pages directory

## NixtLink

To navigate between pages, use NuxtLink component. This component is included
with Nuxt and therefore you dont have to import it. This component is similar to
the `<a>` tag, but instead of `href="/about"` the NuxtLink component uses
`to="/about"`.
		
`<NuxtLink to ="/funpage">Fun Page</NuxtLink>`

## Links to other web pages

Use NuxtLink for in site pages, or and `<a>` tag for external pages

`<a href="https://google.com">A small search engine</a>`
