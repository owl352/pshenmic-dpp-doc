## Welcome to the pshenmic-dpp wiki!

pshenmic-dpp is a JavaScript module that provides lightweight bindings for rs-dpp, enabling the use of the Dash Platform
Protocol in any web application or service.

A key feature of this module is that if you only need a small part of it,
you don't have to include all the bindings — you can manually [build](./Building) the module by editing only `lib.rs`, pulling in just
the components you need along with their minimal dependencies. The module also preserves the structure of rs-dpp as much
as possible.
