testing npm dependency resolution

- npm built-in deduping (at npm install) only avoids duplicating depedencies of the same version when they have a common parent. If they are at the same level in the tree, even if the same exact version, they will be duplicated.

- The `npm dedupe` command only works for deps in the npm registry - it will break if you point to deps on github