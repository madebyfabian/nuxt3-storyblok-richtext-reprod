# Nuxt 3 Richtext Production SSR Issue Reprod
See https://github.com/MarvinRudolph/storyblok-rich-text-renderer/issues/21

This repo was created by following the official cli `npx nuxi init nuxt3-app` nuxi init command.

## Development
To get it running, `npm install`. Then, run `npm run build` and then `npm run preview`. 
You now see a production build of nuxt3 in ssr mode at `http://localhost:3000`. If you open it in your browser, you can now see the error mentioned in the issue. It goes away when wrapping the richtext element with `<ClientOnly>` like this:

```
<ClientOnly>
  <RichTextRenderer :document="doc" />
</ClientOnly>
```
