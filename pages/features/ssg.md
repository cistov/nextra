# Next.js SSG

With Next.js, you can pre-render your page using [Static Generation \(SSG\)](https://nextjs.org/docs/basic-features/pages#static-generation-recommended). Your pages will be generated at build time and statically served to visitors. It can also be cached by a CDN to maximize the performance.

This is supported by Nextra too. Here's an example:

import { useSSG } from 'nextra/ssg'

export const getStaticProps = \({ params }\) =&gt; { return fetch\(`https://api.github.com/repos/shuding/nextra`\) .then\(\(res\) =&gt; res.json\(\)\) .then\(\(repo\) =&gt; \({ props: { // We add an `ssg` field to the page props, // which will be provided to the Nextra `useSSG` hook. ssg: { stars: repo.stargazers\_count, }, }, // The page will be considered as stale and regenerated every 60 seconds. revalidate: 60, }\)\) }

export const Stars = \(\) =&gt; { // Get the data from SSG, and render it as a component. const { stars } = useSSG\(\) return **{stars}** }

 Nextra has stars on GitHub!

The number above was generated at build time via `getStaticProps`. With [Incremental Static Regeneration](https://nextjs.org/docs/basic-features/data-fetching#incremental-static-regeneration) enabled, it will keep up to dated.

Here's the MDX code for the example above:

```javascript
import { useSSG } from 'nextra/ssg'

export const getStaticProps = ({ params }) => {
  return fetch(`https://api.github.com/repos/shuding/nextra`)
    .then((res) => res.json())
    .then((repo) => ({
      props: {
        // We add an `ssg` field to the page props,
        // which will be provided to the Nextra `useSSG` hook.
        ssg: {
          stars: repo.stargazers_count,
        },
      },
      // The page will be considered as stale and regenerated every 60 seconds.
      revalidate: 60,
    }))
}

export const Stars = () => {
  // Get the data from SSG, and render it as a component.
  const { stars } = useSSG()
  return <strong>{stars}</strong>
}


Nextra has <Stars /> stars on GitHub!
```

