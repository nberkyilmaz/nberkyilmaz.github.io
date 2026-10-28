# nberkyilmaz.com

The landing page for [nberkyilmaz.com](https://nberkyilmaz.com), and the repository that holds the
domain.

GitHub Pages serves this repository at the root of the domain, and every other project site on the
account beneath it, at its repository's name:

| Repository | Served at |
| --- | --- |
| this one | <https://nberkyilmaz.com/> |
| [departure-brief](https://github.com/nberkyilmaz/departure-brief) | <https://nberkyilmaz.com/departure-brief/> |
| [hours-to-go](https://github.com/nberkyilmaz/hours-to-go) | <https://nberkyilmaz.com/hours-to-go/> |

So a project needs nothing of its own to appear here: publish it with GitHub Pages and build it for
the path `/<repository>/`. Turning a project's Pages off takes it off the domain.

The domain is set in this repository's Settings → Pages. DNS is at Cloudflare: four A and four AAAA
records on the apex pointing at GitHub Pages, `www` as a CNAME to `nberkyilmaz.github.io`, all DNS
only. The MX and TXT records on the apex are the domain's email and are separate.

This page is a placeholder for a fuller portfolio: plain HTML, no build step.
