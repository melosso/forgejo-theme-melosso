# Melosso for [Forgejo](https://forgejo.org/)

To install this in your Forgejo instance, you'll have to take [theme-melosso.css](https://www.google.com/search?q=./theme-melosso.css) (auto dark/light) and/or [theme-melosso-dark.css](https://www.google.com/search?q=./theme-melosso-dark.css) and/or [theme-melosso-light.css](https://www.google.com/search?q=./theme-melosso-light.css) and put them into your forgejo custom directory. Specifically, drop them right into `custom/public/assets/css/`. If that path doesn't exist yet, just create the folders.

> Melosso is based on the original [Dracula theme](https://github.com/axxy/forgejo-theme-dracula) by Taylor C. Richberger.

Anyway, `theme-melosso.css` is the auto theme, which switches with the user's preferred color scheme. It's a good default choice.

Next, you'll have to modify your [app.ini](https://forgejo.org/docs/next/admin/config-cheat-sheet/#ui-ui) so Forgejo actually knows the themes are there. Open your `app.ini` file and look for the `[ui]` section. You just need to append the new themes to your `THEMES` list.

If you want the auto theme to be the default for everyone right out of the gate, update the `DEFAULT_THEME` variable while you are at it. It should look something like this:

```ini
[ui]
DEFAULT_THEME = melosso
THEMES = forgejo-auto, forgejo-light, forgejo-dark, melosso, melosso-dark, melosso-light
```

Save the file and restart your Forgejo instance (e.g. `sudo systemctl restart forgejo`) so the changes take effect.
