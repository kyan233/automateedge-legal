# AutomateEdge — app policies

Public legal pages for AutomateEdge apps, served by GitHub Pages at
**<https://legal.automateedge.ai>**.

This repo is public **on purpose** — Apple requires every app's privacy policy to
be reachable at a public URL, and re-checks that URL on every submission and
update. Nothing secret belongs here. App source code lives in its own private
repo.

## Live URLs

| App | Policy URL |
| --- | --- |
| Lockout | <https://legal.automateedge.ai/lockout/> |

## Adding an app

1. `cp -r _template <appname>`
2. Open `<appname>/index.html` and replace every `{{PLACEHOLDER}}`.
3. Delete any section that does not apply. Do **not** leave a section in that
   claims something untrue — reviewers and users both read this.
4. Add a row to the list in `index.html` and to the table above.
5. Commit and push. Pages redeploys in about a minute.

The contact address uses `+` routing — `kyansukhram+<appname>@automateedge.ai`
lands in the same inbox but tells you which app the sender is writing about.
Google Workspace delivers these with no setup required.

## Styling

All pages share `style.css`. Edit it once and every app's policy follows. It is
responsive and adapts to light and dark mode.

## DNS

`CNAME` pins the custom domain. The matching DNS record at Namecheap is:

```
Type: CNAME   Host: legal   Value: kyan233.github.io.
```

Do not delete `CNAME` — losing it drops the custom domain and breaks every
policy link already filed with Apple.
