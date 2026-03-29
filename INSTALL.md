# Melosso for [Forgejo](https://forgejo.org/)

To install this in your Forgejo instance, you'll have to take [theme-melosso.css](./theme-melosso.css) (auto dark/light) and/or [theme-melosso-dark.css](./theme-melosso-dark.css) and/or [theme-melosso-light.css](./theme-melosso-light.css) and put them into your forgejo custom/public/assets/css directory, then you'll have to modify your [app.ini](https://forgejo.org/docs/next/admin/config-cheat-sheet/#ui-ui) to contain it in the themes list.

> Melosso is based on the original [Dracula theme](https://github.com/axxy/forgejo-theme-dracula) by Taylor C. Richberger.

Anyway, `theme-melosso.css` is the auto theme, which switches with the user's preferred color scheme. It's a good default choice.

You can examine this forge's deployment for information:

* [The Containerfile shows how the themes are downloaded and where they're put.](https://github.com/axxy/forge.axfive.net/blob/main/Containerfile)
* [The download-themes.sh script shows how the themes are downloaded and installed](https://github.com/axxy/forge.axfive.net/blob/main/download-themes.sh)
* [The app.ini shows how it is set up along with other themes and set to the default](https://github.com/axxy/forge.axfive.net/blob/main/app.ini)
