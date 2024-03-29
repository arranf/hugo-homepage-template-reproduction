This repo is to demonstrate an issue with Hugo version `hugo v0.124.1-db083b05f16c945fec04f745f0ca8640560cf1ec+extended darwin/arm64` where it fails to find and use the template for the home page despite `layouts/index.html` existing.

To reproduce this the key elements appear to be:

* Having a `/layouts/index.html` template
* Configuring `taxonomies` so that at least one of the key value pairs has an array as the value in hugo.toml
* **Not** having a `/content/_index.md`
