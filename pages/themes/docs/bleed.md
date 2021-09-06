# Bleed

A built-in component provided by `nextra-theme-docs`.

## Example

import Bleed from 'nextra-theme-docs/bleed'

When wrapping your content with `<Bleed>`, it will be slightly wider than the container and will overflow on both sides.

 \_There is nothing to writing. All you do is sit down at a typewriter and \*\*bleed\*\*.\_ — Ernest Hemingway

It providers a better reading experience when you want to present some graphical information, which normally looks nicer in a larger size.

For example you can put text, image, video or any component inside:

You can even make it full-bleed using `<Bleed full>`:

 !\[Landscape\]\(https://source.unsplash.com/eaxwP9J\_V6s/1600x398\)

## Usage

```text
import Bleed from 'nextra-theme-docs/bleed'

<Bleed>Hey, I can use **Markdown** syntax here.</Bleed>

<Bleed full>
  ![Landscape](https://source.unsplash.com/eaxwP9J_V6s/1600x398)
</Bleed>

<Bleed full>
  <iframe
    src="https://codesandbox.io/embed/swr-states-4une7"
    width="100%"
    height="500px"
    title="SWR-States"
  ></iframe>
</Bleed>
```

