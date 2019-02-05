# rollup-reserved-word-issue

Reproduce issue in rollup. When flattening imports javascript reserved words should be escaped.

`* as module` gets flattened into actually used exports. Which is usually fine but the
resulting names must not collide with anything in scope OR reserved javascript words.

It seems rollup does not check for the latter.


# repo

npx rollup index.js
