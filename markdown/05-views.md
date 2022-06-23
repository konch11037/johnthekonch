# Views

The Views section describes all you need to know to configure data and views for a specific route in your Nuxt Application. Views consist of an app template, a layout, and the actual page.

## Pages 

Every Page component is a Vue component but Nuxt adds special attributes and functions to make the development of your application as easy as possible.

```
<template>
  <h1 class="red">Hello World</h1>
</template>

<script>
  export default {
    head() {
      // Set Meta Tags for this Page
    }
    // ...
  }
</script>

<style>
  .red {
    color: red;
  }
</style>
```

## Layouts

Layouts are a great help when you want to change the look and feel of your Nuxt app. For example you want to include a sidebar or have distinct layouts for mobile and desktop.

### Default layout

You can define a default layout by adding a default.vue file inside the layouts
directory. This will be used for all pages that dont have a layout specified.
The only thing you need to include in the layout is the <Nuxt /> component which
renders the page component.

```
<template>
  <Nuxt />
</template>
```

### Custom Layout

You can create custom layouts by adding a .vue file to the layouts directory. In
order to use the costom layout you need to set the layout property in the page
component where you want to yse that layout. The value will be the name of the
custom layout that you have created.

To create a blog layout add a blog.vue file to your layouts directory
`layouts/blog.vue`

```
<template>
  <div>
    <div>My blog navigation bar here</div>
    <Nuxt />
  </div>
</template>
```

^^ this needs t have the nuxt component.

We then yse the layout property with the value of 'blog' in the page where we
want that layout to be used. 

```
<template>
  <!-- Your template -->
</template>
<script>
  export default {
    layout: 'blog'
    // page component definitions
  }
</script>
```

### Error Page

The error page is a page component which is always displayed when an error occurs (that does not happen while server-side rendering).

Although this file is placed in the layouts folder, it should be treated as a page.

As mentioned above, this layout is special, since you should not include the <Nuxt/>  component inside its template. You must see this layout as a component displayed when an error occurs (404, 500, etc.). Similar to other page components, you can set a custom layout for the error page as well in the usual way.

You can customize the error page by adding a layouts/error.vue file:

```
<template>
  <div>
    <h1 v-if="error.statusCode === 404">Page not found</h1>
    <h1 v-else>An error occurred</h1>
    <NuxtLink to="/">Home page</NuxtLink>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error' // you can set a custom layout for the error page
  }
</script>
```
