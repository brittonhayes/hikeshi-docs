---
description: Getting up and running with the application and it's database.
---

# Installation

## Installing the application

> Getting started on OSX, Linux, and Windows is easy with the [homebrew tap](https://brew.sh/) or Scoop Bucket. While we recommend the homebrew approach for local development/usage, you can also install Hikeshi with `go get` or `git clone` if you prefer those routes.

{% tabs %}
{% tab title="Homebrew" %}
```bash
brew tap brittonhayes/hikeshi-tap
brew install hikeshi
hikeshi --help
```
{% endtab %}

{% tab title="Scoop" %}
```
scoop bucket add hikeshi https://github.com/brittonhayes/hikeshi-scoop.git
```
{% endtab %}

{% tab title="Source" %}
```bash
gh repo clone brittonhayes/hikeshi
brew install gobuffalo/tap/buffalo
buffalo build
hikeshi --help
```
{% endtab %}
{% endtabs %}

## Installing the database

{% tabs %}
{% tab title="Homebrew" %}
```bash
brew install postgres
```
{% endtab %}

{% tab title="Docker" %}
```text
docker pull postgres
```
{% endtab %}
{% endtabs %}



