# Hosting with a VPS

If you own a VPS, you can easily host your ModMail instance by doing the following steps.

First of all, make sure you have installed [NodeJS](https://nodejs.org/), [Git](https://git-scm.com/) and [PM2](https://pm2.keymetrics.io/) into your machine.

Then, clone the repository.

```bash
$ git clone https://github.com/ThePhoDit/ModMail
$ cd ModMail
```

If you are on a Linux or MacOS system, run `npm run linux` and if you are on a Windows one, run `npm run windows`. You will be asked to introduce some variables related to the Bot and to the DataBase. If you choose to use mongo, you have to  provide a connection URI to the DB \(you can use Mongo Atlas\).

After that, edit the file  `src/config.ts`with Vim, Nano or other text editor and fill it following the indications there \(see the [parameters table](../utility/config-file-parameters.md)\).

At last, do:

```text
$ npm run build
$ pm2 start prod/index.js --name modmail
```

{% hint style="success" %}
Great! Your bot is already hosted.
{% endhint %}

