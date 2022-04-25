# mdx

## MDX

With Nextra, all your `.md` and `.mdx` files under **the pages directory** will be rendered with [MDX](https://mdxjs.com/about), it's an advanced `Markdown` format with React component support.



<details>

<summary>Title </summary>

Expandable content

</details>

## Heading

{% tabs %}
{% tab title="First Tab" %}
Content 1
{% endtab %}

{% tab title="Second Tab" %}
Content 2
{% endtab %}
{% endtabs %}

You can use import and use [Reac](feature-x.md)t <mark style="color:red;">components</mark> inside your Markdown files like this:

```
import Callout from 'nextra-theme-docs/callout'

**Markdown With React Components**

<Callout emoji="✅">
  **MDX** (the library), at its core, transforms MDX (the syntax) to JSX.
  It receives an MDX string and outputs a _JSX string_. It does this by parsing
  the MDX document to a syntax tree and then generates a JSX document from that tree. 
</Callout>
```

Generates:

import Callout from 'nextra-theme-docs/callout'

&#x20;\*\*Markdown With React Components\*\* \*\*MDX\*\* (the library), at its core, transforms MDX (the syntax) to JSX. It receives an MDX string and outputs a \_JSX string\_. It does this by parsing the MDX document to a syntax tree and then generates a JSX document from that tree.

### Heading

## **Hello**, This Is a _Title_ Inside `h1`

\*\*Hello\*\*, This Is a \_Title\_ Inside \`h2\` {/ _using html tag to avoid being rendered in the sidebar_ /}

#### **Hello**, This Is a _Title_ Inside `h3`

**Hello, This Is a Title Inside h4**

**Hello, This Is a Title Inside h5**

**Hello, This Is a Title Inside h6**

### List

1. one
2. two
3. three
4. one
5. two
6. three

### Task List

```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

Renders

* [x] Write the press release
* [ ] Update the website
* [ ] Contact the media

### Syntax Highlighting

Automatica syntax highlighting:

````
```js
console.log('hello, world')
```
````

Renders:

```javascript
console.log('hello, world')
```

You can also add the `highlight=<line|range>` modifier to highlight specific lines:

````
```jsx highlight=4,6-8
import useSWR from 'swr'

function Profile() {
  const { data, error } = useSWR('/api/user', fetcher)

  if (error) return <div>failed to load</div>
  if (!data) return <div>loading...</div>
  return <div>hello {data.name}!</div>
}
```
````

\`\`\`jsx highlight=4,6-8 import useSWR from 'swr'

function Profile() { const { data, error } = useSWR('/api/user', fetcher)

if (error) return failed to load if (!data) return loading... return hello {data.name}! }

````
## Inline Code

You can use \`content\` to wrap inline code content like: `let x = 1`.

## Blockquote

> Where some people measure progress in answers-right per test or tests-passed per year, we are more interested in Sistine-Chapel-Ceilings per Lifetime.
>
> — Alan Kay, A Personal Computer for Children of All Ages

Nested quotes:

> > Where some people measure progress in answers-right per test or tests-passed per year, we are more interested in Sistine-Chapel-Ceilings per Lifetime.
> >
> > — Alan Kay, A Personal Computer for Children of All Ages
>
> This is **great**.
>
> — Shu Ding.

## Table

| Syntax        | Description |   Test Text |
| :------------ | :---------: | ----------: |
| Header        |    Title    | Here's this |
| Paragraph     |    Text     |    And more |
| Strikethrough |             |    ~~Text~~ |

## React Components

React components and Markdown can be **mixed together**, for instance:

```markdown
> <Callout>
>   Give [**Nextra**](https://github.com/shuding/nextra) a star!
> </Callout>
````

Renders:

> &#x20;Give \[\*\*Nextra\*\*]\(https://github.com/shuding/nextra) a star!
