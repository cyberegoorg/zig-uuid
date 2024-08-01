# zig-uuid

[![CI][ci-shd]][ci-url]
[![CD][cd-shd]][cd-url]
[![DC][dc-shd]][dc-url]
[![LC][lc-shd]][lc-url]

## Zig implementation of [all seven UUID versions](https://www.ietf.org/archive/id/draft-peabody-dispatch-new-uuid-format-04.html).

### :rocket: Usage

- Add `uuid` dependency to `build.zig.zon`.

```sh
zig fetch --save https://github.com/tensorush/zig-uuid/archive/<git_tag_or_commit_hash>.tar.gz
```

- Use `uuid` dependency in `build.zig`.

```zig
const uuid_dep = b.dependency("uuid", .{
    .target = target,
    .optimize = optimize,
});
const uuid_mod = uuid_dep.module("Uuid");
<compile>.root_module.addImport("Uuid", uuid_mod);
```

<!-- MARKDOWN LINKS -->

[ci-shd]: https://img.shields.io/github/actions/workflow/status/tensorush/uuid/ci.yaml?branch=main&style=for-the-badge&logo=github&label=CI&labelColor=black
[ci-url]: https://github.com/tensorush/uuid/blob/main/.github/workflows/ci.yaml
[cd-shd]: https://img.shields.io/github/actions/workflow/status/tensorush/uuid/cd.yaml?branch=main&style=for-the-badge&logo=github&label=CD&labelColor=black
[cd-url]: https://github.com/tensorush/uuid/blob/main/.github/workflows/cd.yaml
[dc-shd]: https://img.shields.io/badge/click-F6A516?style=for-the-badge&logo=zig&logoColor=F6A516&label=doc&labelColor=black
[dc-url]: https://tensorush.github.io/uuid
[lc-shd]: https://img.shields.io/github/license/tensorush/uuid.svg?style=for-the-badge&labelColor=black
[lc-url]: https://github.com/tensorush/uuid/blob/main/LICENSE
