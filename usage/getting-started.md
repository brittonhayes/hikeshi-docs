---
description: How to run Hikeshi for the first time.
---

# Getting Started

## The Database

> You can start the database however you prefer or even provide a remote DB url and not start a database locally. But in the event that you do decide to spin up postgres on your local environment, Docker is the easiest way to get up and running with a clean slate, so that's what we recommend.

### Start it up

{% tabs %}
{% tab title="Docker" %}
```text
docker run --name db -e \
POSTGRES_USER=hikeshi \
POSTGRES_DATABASE=hikeshi_development \
POSTGRES_PASSWORD=postgres \
--ports 1234:5432
-d postgres
```
{% endtab %}
{% endtabs %}

Once you've gotten the database up and running, we can have hikeshi build the tables, rows, and add a default user.

### Scaffolding

{% tabs %}
{% tab title="" %}
```

```
{% endtab %}

{% tab title="Required" %}
```text
hikeshi migrate
hikeshi task db:seed:users
```
{% endtab %}
{% endtabs %}

At this point your database should be up and running with a default user and a placeholder incident. You're now ready to start the application. 

## The Application

### Start it up

{% tabs %}
{% tab title="Default" %}
> The default run mode of the hikeshi binary is Dev. Developer mode runs the application with hot asset reloading and detailed error messages so you can see if your environment is in working order. This is **NOT** recommended for production usage.

```text
hikeshi
```
{% endtab %}

{% tab title="Production Mode" %}
### Production mode

> Developer mode runs the application without debug logs and requires a valid SSL certificate.

```text
GO_ENV=production hikeshi
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
For more information on available environment variables, see the [Buffalo Config vars documentation](https://gobuffalo.io/en/docs/getting-started/config-vars).
{% endhint %}

## Success!

If you followed the above steps without an hiccups, you should be able to log in to Hikeshi at [http://localhost:3000](http://localhost:3000)



