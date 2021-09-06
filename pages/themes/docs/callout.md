# Callout Component

A built-in component provided by `nextra-theme-docs`.

import Callout from 'nextra-theme-docs/callout'

## Example

 A \*\*callout\*\* is a short piece of text intended to attract attention.

## Usage

### Default

 \*\*Space Invaders\*\* is a 1978 shoot 'em up arcade game developed by Tomohiro Nishikado.

```text
import Callout from 'nextra-theme-docs/callout'

<Callout emoji="👾">
  **Space Invaders** is a 1978 shoot 'em up arcade game developed by Tomohiro
  Nishikado.
</Callout>
```

### Warning

 This API will be deprecated soon.

```text
import Callout from 'nextra-theme-docs/callout'

<Callout type="warning" emoji="⚠️">
  This API will be deprecated soon.
</Callout>
```

### Error

 This is a dangerous feature that can cause everything to explode.

```text
import Callout from 'nextra-theme-docs/callout'

<Callout type="error" emoji="️🚫">
  This is a dangerous feature that can cause everything to explode.
</Callout>
```

