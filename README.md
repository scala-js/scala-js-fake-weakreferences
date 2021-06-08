# scalajs-fake-weakreferences

`scalajs-fake-weakreferences` provides compatibility stubs for `java.lang.ref.*` APIs in Scala.js.
It preserves the support that was available in Scala.js core previous to v1.6.0.

The various `Reference`s provided by `scalajs-fake-weakreferences` do not behave correctly.
They always act as strong references.

`scalajs-fake-weakreferences` should only be used if upgrading to Scala.js v1.6.0+ causes linking errors about `java.lang.ref.*` in an existing application.
New applications should avoid this library.

## Usage

Add the following dependency to your project settings:

```scala
libraryDependencies += "org.scala-js" %%% "scalajs-fake-weakreferences" % "1.0.0-SNAPSHOT"
```

When using a `crossProject`, add the above in `.jsSettings(...)`.

You can then use the classes defined in `java.lang.ref.*`.
Keep in mind that they will hold *strong* references, which will prevent the target objects from beging garbage-collected.

## License

`scalajs-fake-weakreferences` is distributed under the [Apache 2.0 license](./LICENSE.txt), like Scala.js itself.
