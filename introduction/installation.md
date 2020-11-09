---
description: Getting up and running with the application and it's database.
---

# Installation

## Installing the application

> Getting started on OSX is easy with the [homebrew tap](https://brew.sh/). While we recommend the homebrew approach for local development/usage, you can also install Hikeshi with `go get` or `git clone` if you prefer those routes.

{% tabs %}
{% tab title="Homebrew" %}
```bash
brew tap brittonhayes/hikeshi-tap
brew install brittonhayes/hikeshi-tap
hikeshi --help
```
{% endtab %}

{% tab title="Source" %}
```bash
git clone git@github.com:brittonhayes/hikeshi.git
hikeshi --help
```
{% endtab %}

{% tab title="Wget + jq" %}
```bash
wget -q -nv -O- https://api.github.com/repos/brittonhayes/hikeshi/releases/latest 2>/dev/null | jq -r '.assets[] | select(.browser_download_url | contains("linux-amd64")) | .browser_download_url'
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

{% tab title="Linux" %}
```text
sudo apt-get install postgresql
```
{% endtab %}

{% tab title="Docker" %}
```text
docker pull postgres
```
{% endtab %}
{% endtabs %}



