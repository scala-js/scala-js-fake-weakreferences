# scalajs-fake-weakreferences

`scalajs-fake-weakreferences` provides compatibility stubs for `java.lang.ref.*` APIs in Scala.js.
It preserves the support that was available in Scala.js core previous to v1.6.0.

The various `Reference`s provided by `scalajs-fake-weakreferences` do not behave correctly.
They always act as strong references.

`scalajs-fake-weakreferences` should only be used if upgrading to Scala.js v1.6.0+ causes linking errors about `java.lang.ref.*` in an existing application.
New applications should avoid this library.

## License

`scalajs-fake-weakreferences` is distributed under the [Apache 2.0 license](./LICENSE.txt), like Scala.js itself.
