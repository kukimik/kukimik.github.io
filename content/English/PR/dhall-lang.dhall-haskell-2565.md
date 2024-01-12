#  dhall-docs: render standalone text files as preformatted text \#2565 

https://github.com/dhall-lang/dhall-haskell/pull/2565

* `git` automatically converts betweem DOS and Unix newlines (CRLF/LF, `\r\n`/`\n`) in text files
  * this may be overriden per-file: `.gitattributes` (see https://git-scm.com/docs/gitattributes)
* this may break golden tests, see https://hackage.haskell.org/package/tasty-golden-2.3.5/docs/Test-Tasty-Golden.html
