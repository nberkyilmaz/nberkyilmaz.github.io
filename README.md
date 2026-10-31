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

The page is plain HTML with no build step.

## The résumé

`resume.pdf`, served at <https://nberkyilmaz.com/resume.pdf>, is a copy of `out/resume.pdf` from the
private `resume` repository: the build of `resume.tex`, which has no phone number. Copy it again
whenever the résumé changes. Never copy `Berk_Yilmaz_Resume.pdf`, the version for applying, which
has the phone number.

## The live METAR

The hero shows Toronto Island's latest METAR, read from
[Departure Brief's relay](https://github.com/nberkyilmaz/departure-brief/tree/master/apps/relay)
at `/awc/metar?ids=CYTZ&format=json`. The relay only answers pages on its `ALLOWED_ORIGINS` list,
which includes `https://nberkyilmaz.com`. If the relay doesn't answer, or the report is more than
three hours old, the card is removed and the hero looks as it would without it.

Every number on the page comes from the résumé repository's `achievements.md`, where each one is
traced to its source. Clients stay unnamed.
