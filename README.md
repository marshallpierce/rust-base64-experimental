A place to experiment with a better design for a base64 library.

Some goals I'm thinking about:

- Pluggable implementations: let the user choose between scalar code and cpu-specific vectorized implementations.
- No line wrapping support, at least not built in to a `Config`. It greatly complicates the code, and can probably be done after the fact.
- Bytes, not strings. Let the user decide if they want to pay the cost of UTF8-ing safely or not.
- Minimal or no defaults to keep the API surface small. If the user ends up always using the same config, let them make a tiny helper method in their project.
- `no_std` support
