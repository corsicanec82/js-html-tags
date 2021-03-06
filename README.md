# js-html-tags

[![github action status](https://github.com/hexlet-components/js-html-tags/workflows/Node%20CI/badge.svg)](https://github.com/hexlet-components/js-html-tags/actions)

## Install

```sh
npm install @hexlet/html-tags
```

## Usage example

```javascript
import {
  node, addChild, make, append, toString, hasChildren,
} from '@hexlet/html-tags';

const p = node('p', 'paragraph');
const ul = node('ul');
const ul2 = addChild(ul, node('li', 'body'));
const ul3 = addChild(ul2, node('li', 'another body'));
const dom1 = make();
const dom2 = append(dom1, p);
const dom3 = append(dom2, ul3);

toString(dom3);
// '<p>paragraph</p><ul><li>body</li><li>another body</li></ul>';

getName(p); // 'p'
getValue(p); // 'paragraph'
hasChildren(p); // false
```

For more information, see the [Full Documentation](https://github.com/hexlet-components/js-html-tags/tree/master/docs)
