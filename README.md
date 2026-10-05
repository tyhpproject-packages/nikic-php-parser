<!-- tyhp-readme:start -->
# tyhpdef/nikic-php-parser

Tyhp type definitions for `nikic/php-parser` `5.9.0`.

```bash
composer require --dev tyhpdef/nikic-php-parser:5.9.0
```

This is a metapackage. Composer also installs `tyhpdef/nikic-php-parser-impl` (type files).
Require **this** name, not `tyhpdef/nikic-php-parser-impl`.

See https://tyhplang.com.

## Maintain `nikic/php-parser`? Ship the types yourself

If you are a Packagist maintainer of `nikic/php-parser`, you can take over these
types.

Copy `_tyhpdef/` from **`tyhpdef/nikic-php-parser-impl`** (Apache-2.0; keep the `NOTICE`).
Then either:

1. **Bundle** the files in `nikic/php-parser` and set `extra.tyhp.package` on
   that `composer.json`, plus
   `"replace": { "tyhpdef/nikic-php-parser": "self.version" }`, or
2. **Publish a sibling** types package under your vendor, versioned with
   `nikic/php-parser` (same `X.Y.Z`). Set `extra.tyhp.package` there,
   `require` `nikic/php-parser` with a real constraint,
   `"replace": { "tyhpdef/nikic-php-parser": "self.version" }`, and set
   `extra.tyhp.tyhpdef` on `nikic/php-parser` to your sibling’s Composer name.

Ship that to Packagist first, then open an issue:

https://github.com/tyhpproject/tyhp-runtime-src/issues/new?template=tyhpdef-ownership.yml

We verify Packagist ownership and that the types parse and cover the PHP
API, then stop publishing community tags for those versions. We do not
transfer the `tyhpdef/nikic-php-parser` Packagist name.

Full process: `TYHPDEF_OWNERSHIP.md` in
https://github.com/tyhpproject/tyhp-runtime-src
<!-- tyhp-readme:end -->
