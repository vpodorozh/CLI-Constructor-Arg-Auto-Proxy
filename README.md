---
title: [metapackage] Cli Constructor Arg Auto Proxy  
keywords: CLI, Proxy, ObjectManager  
author: Vlad Podorozhnyi  
send_questions_to: vpodorozh@gmail.com | vlad.podorozhnyi@run-as-root.sh  
category: System
---
![Magento 2](https://img.shields.io/badge/Magento-2.4.*-orange)
![PHP](https://img.shields.io/badge/php-7.4-blue)
![composer](https://shields.io/badge/composer-v2-darkgreen)
![packagist](https://img.shields.io/badge/packagist-f28d1a)

## \[metapackage\] Cli Constructor Arg Auto Proxy

<br />
<div align="center">
  <img src="images/logo.png" alt="Logo" width="100" height="80">

<h3 align="center">Magento 2 - Auto Proxy to CLI class arguments</h3>

  <p align="center">
    Automatically injects Proxy for any argument defined in CLI command class constructor.
    <br />
  </p>
</div>

## About The Project

### Purpose:
* speed up `php bin/magento` command execution;
* eliminate `.flag table not found` issues while installation of your project with fresh database (usually used with integration tests) - caused by not using Proxy in CLI of 3rd parties.

### Structure:
Project consists of 3 packages:
* **Magento 2 Component:** `vpodorozh/cli-construct-arg-auto-proxy-component` - provides entry point to Magento via global DI config. See [README](component/README.md);
* **Library:** `vpodorozh/cli-construct-arg-auto-proxy-lib` - contains main logic about Proxy injection. See [README](lib/README.md);
* **Metapackage:** `vpodorozh/cli-construct-arg-auto-proxy-meta` - main package to use, orchestrate project versions.

## Getting Started

### Prerequisites
* Magento v2.4.* and upper
* composer v2 and upper

### Installation

```bash
# flush cache first
php bin/magento cache:flush
# then require a package
composer req vpodorozh/cli-construct-arg-auto-proxy-meta:*
```

## Roadmap

- [x] MVP release
- [x] Documentation
- [ ] Unit tests coverage
- [ ] Static tests coverage
  - [ ] php linting
  - [ ] phpcs
  - [ ] phpmd
  - [ ] phpstan
- [ ] Integration tests coverage
- [ ] Pipelines tests automation
    - [ ] Static tests
    - [ ] Unit tests
    - [ ] Integration tests
    - [ ] Magento multiversions tests

## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

## Contact

Vlad Podorozhnyi  
Twitter: [![@vpodorozh](https://img.shields.io/twitter/url?style=social&url=https%3A%2F%2Ftwitter.com%2Fvpodorozh)](https://twitter.com/vpodorozh)  
Email: `vpodorozh@gmail.com`
