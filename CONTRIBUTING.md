---
layout: page
title: Contribute
---

## Structure

Each oneliner is defined in a file in the [`_oneliners/`] folder named as `<tool name>.md`, such file consists only of a [YAML] front matter which describes the command and its attributes.

The full syntax is the following:

```
---
description: Description of what the command does.

  Command Reference:

  	Target IP: 10.10.10.1

  	Domain: test.local

  	Username: john

  	Password: password123

command: |
  put command here
items:
  - ITEM 1
  - ITEM 2
  ... 
services:
  - SERVICE
  ...
OS:
  - OS
  ...
attack_types:
  - ATTACK TYPE
references:
  - LINK
  ...
---
```

Where `ITEM` is one of the values described in the [`_data/items.yml`] file, `SERVICE` is one of the values described in the [`_data/services.yml`] file, `OS` is one of the values described in the [`_data/OS.yml`] file, `ATTACK_TYPE` is one of the values described in the [`_data/attack_types.yml`] file, and `LINK` is a link to download the related tool for that command as well as links to any other relevant information about what the command is doing. 

Feel free to use any file in the [`_oneliners/`] folder as an example.

[YAML]: http://yaml.org/
[`_oneliners/`]: https://github.com/hackerbible/hackerbible.github.io/tree/main/_oneliners
[`_data/services.yml`]: https://github.com/hackerbible/hackerbible.github.io/blob/main/_data/services.yml
[`_data/items.yml`]: https://github.com/hackerbible/hackerbible.github.io/blob/main/_data/items.yml
[`_data/OS.yml`]: https://github.com/hackerbible/hackerbible.github.io/blob/main/_data/OS.yml
[`_data/attack_types.yml`]: https://github.com/hackerbible/hackerbible.github.io/blob/main/_data/attack_types.yml
