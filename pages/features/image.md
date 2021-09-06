# Next.js Image

You can use [Next.js Image](https://nextjs.org/docs/basic-features/image-optimization) directly in MDX.

If the `demo.png` file is located at `/public/demo.png`, you can use the code below to display it:

```text
import Image from 'next/image'

<Image src="/demo.png" alt="Hello" width={500} height={500} />
```

## Static Image

import Callout from 'nextra-theme-docs/callout'

 You need to opt-in to this feature by enabling \[\`unstable\_staticImage: true\`\]\(/get-started\#create-manually\).

Nextra also supports automatic static image imports, you no longer need to specify the width and height of the image manually, and you can directly use the Markdown syntax to display the same image:

```text
![Hello](../../public/demo.png)
```

With Next.js Image, there will be no layout shift, and a beautiful blury placeholder will be shown by default when loading the images:

![Nextra](../../.gitbook/assets/og.png)

