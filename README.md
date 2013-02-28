libtoml
=======

Fast C parser using Ragel to generate the state machine.

Currently targetted at toml 3f4224ecdc4a65fdd28b4fb70d46f4c0bd3700aa, with the exception of UTF8 strings.

Usage
=====

```c
#include <toml.h>

struct toml_node *root;
struct toml_node *node;

toml_init(&root);
toml_parse(toml_root, buf, len);

node = toml_get(toml_root, "foo.bar");

toml_dump(toml_root, stdout);
toml_free(root);
```

TODO
====

Tests
UTF8 support
