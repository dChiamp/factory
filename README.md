# factory

The Funkhaus component Factory - a proof of concept for an upcoming component marketplace

Explain what this repo is for. Mention James Lee.

## How to install Storybook

Install instructions go here.

## How to accept a Component Request

## How to submit a finished Component for review

## How to get paid

Venmmo or PayPal

## Timeline

Most components should take between 2-4 hours to complete. So please don't accept a component unless you plan on finishing it within the next 48 hours. If more than 48 hours pass since starting on a component, you will be removed from the component and it's free for someone else to claim.

### Code styleguide and expectations

- No outside libraries without asking. Here is a whitelist of approved ones:
  - lodash: https://lodash.com/
    - ([Be sure to only import functions you need](https://github.com/funkhaus/fuxt/blob/master/components/WpImage.vue#L41))
  - vue-prlx: http://vue-prlx.surge.sh/
- Sorry, no Tailwind (yet).
- What about animations?
  - Almost all transitions you'll be asked to do can be completed with the Vue `<transition>` component and CSS or JS hooks.

Explain included Linting, Prettier config etc..

### Fonts

How to give out fonts to Devs? Webfontloader in storybook?

### Funkhaus best practices

Explain this: https://docs.google.com/presentation/d/1xMqvylzoIwpEgwFEpXI8it_HGo7BUGrt8h65E0nvEQo/edit?usp=sharing

### Mock data

All our data generally comes our of WordPress using the WP-GQL. But we've setup some ways to access the data easily.

#### Option 1 - Import file

The file `db.json` found in the root of this repo can be downloaded, and used in your components like this:

```
<template>
    <example-component :prop-name="api.pages"/>
<template>

<script>
import mockApi from "~/assets/db.json"
export default {
    data() {
        return {
            api: mockApi
        }
    }
}
</script>
```

#### Option 2 - API endpoints

Alternatively, you can access this the mock API via Typicode's JSON server like so:

- https://my-json-server.typicode.com/funkhaus/factory/image
- https://my-json-server.typicode.com/funkhaus/factory/images
- https://my-json-server.typicode.com/funkhaus/factory/images/cG9zdDoyODk=
- https://my-json-server.typicode.com/funkhaus/factory/page
- https://my-json-server.typicode.com/funkhaus/factory/pages

These endpoints just map to the contents of `db.json`, so feel free to dig into that file to find what you need.

## References

Include some good things to read here.

## TODO

- Finish this documentation
- Build out GitHub issue tags for things like difficulty level, budget, ready for code review etc.
- Have a “project specification” issue template that defines global things like css vars or maybe design files? In component requests, like to the project spec.
