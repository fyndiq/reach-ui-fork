---
title: VisuallyHidden
description: React component to provide visually hidden text for screen readers
---

- Source: https://github.com/reach/reach-ui/tree/main/packages/visually-hidden
- Origin: https://snook.ca/archives/html_and_css/hiding-content-for-accessibility
- Further reading: https://a11yproject.com/posts/how-to-hide-content/

Provides text for screen readers that is visually hidden. It is the logical opposite of the `aria-hidden` attribute.

In the following example, screen readers will announce "Save" and will ignore the icon; the browser displays the icon and ignores the text.

```jsx
<button>
	<VisuallyHidden>Save</VisuallyHidden>
	<svg aria-hidden width="32" height="32">
		<path d="M16 18l8-8h-6v-8h-4v8h-6zM23.273 14.727l-2.242 2.242 8.128 3.031-13.158 4.907-13.158-4.907 8.127-3.031-2.242-2.242-8.727 3.273v8l16 6 16-6v-8z"></path>
	</svg>
</button>
```

## Installation

From the command line in your project directory, run `npm install @reach/visually-hidden` or `yarn add @reach/visually-hidden`. Then import the component:

```bash
npm install @reach/visually-hidden
# or
yarn add @reach/visually-hidden
```

```js
import { VisuallyHidden } from "@reach/visually-hidden";
```

## Component API

### VisuallyHidden

#### VisuallyHidden Props

| Prop                                   | Type                    | Required |
| -------------------------------------- | ----------------------- | -------- |
| [`as`](#visuallyhidden-as)             | `string` \| `Component` | false    |
| [`children`](#visuallyhidden-children) | `node`                  | true     |

##### VisuallyHidden `as`

`as?: keyof JSX.IntrinsicElements | React.ComponentType`

A string representing an HTML element or a React component that will tell the `VisuallyHidden` what element to render. Defaults to `span`.

<div class="Note">
	<p>
		<strong>NOTE:</strong> Many semantic elements, such as <code>button</code>{" "}
		elements, have meaning to assistive devices and browsers that provide
		context for the user and, in many cases, provide or restrict interactive
		behaviors. Use caution when overriding our defaults and make sure that the
		element you choose to render provides the same experience for all users.
	</p>
</div>

##### VisuallyHidden `children`

`children: React.ReactNode`

The content you want to be visually hidden.