# dom-serializer

fork of [@cheeriojs](https://github.com/cheeriojs)[/dom-serializer](https://github.com/cheeriojs/dom-serializer)

The original package does not work if you are using ES6 modules: [Issue 612](https://github.com/cheeriojs/dom-serializer/issues/612)

<hr/>

Renders a [`domhandler`](https://github.com/fb55/domhandler) DOM node or an array of domhandler DOM nodes to a string.

```ts
import { render } from "dom-serializer";

const html: string = render(dom);
```

# API

## `render`

▸ **render**(`node`: Node \| Node[], `options?`: [_Options_](#Options)): _string_

Renders a DOM node or an array of DOM nodes to a string.

Can be thought of as the equivalent of the `outerHTML` of the passed node(s).

#### Parameters:

| Name      | Type                               | Default value | Description                    |
| :-------- | :--------------------------------- | :------------ | :----------------------------- |
| `node`    | Node \| Node[]                     | -             | Node to be rendered.           |
| `options` | [_DomSerializerOptions_](#Options) | {}            | Changes serialization behavior |

**Returns:** _string_

## Options

### `decodeEntities`

• `Optional` **decodeEntities**: _boolean_

Encode characters that are either reserved in HTML or XML, or are outside of the ASCII range.

**`default`** true

---

### `emptyAttrs`

• `Optional` **emptyAttrs**: _boolean_

Print an empty attribute's value.

**`default`** xmlMode

**`example`** With `emptyAttrs: false`: `&lt;input checked&gt;`

**`example`** With `emptyAttrs: true`: `&lt;input checked=""&gt;`

---

### `selfClosingTags`

• `Optional` **selfClosingTags**: _boolean_

Print self-closing tags for tags without contents.

**`default`** xmlMode

**`example`** With `selfClosingTags: false`: `&lt;foo&gt;&lt;/foo&gt;`

**`example`** With `selfClosingTags: true`: `&lt;foo /&gt;`

---

### `xmlMode`

• `Optional` **xmlMode**: _boolean_ \| _"foreign"_

Treat the input as an XML document; enables the `emptyAttrs` and `selfClosingTags` options.

If the value is `"foreign"`, it will try to correct mixed-case attribute names.

**`default`** false

---

## Ecosystem

| Name                                                          | Description                                             |
| ------------------------------------------------------------- | ------------------------------------------------------- |
| [htmlparser2](https://github.com/fb55/htmlparser2)            | Fast & forgiving HTML/XML parser                        |
| [domhandler](https://github.com/fb55/domhandler)              | Handler for htmlparser2 that turns documents into a DOM |
| [domutils](https://github.com/fb55/domutils)                  | Utilities for working with domhandler's DOM             |
| [css-select](https://github.com/fb55/css-select)              | CSS selector engine, compatible with domhandler's DOM   |
| [cheerio](https://github.com/cheeriojs/cheerio)               | The jQuery API for domhandler's DOM                     |
| [dom-serializer](https://github.com/cheeriojs/dom-serializer) | Serializer for domhandler's DOM                         |

---

LICENSE: MIT
