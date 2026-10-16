# vajska.rs

Site of the selo network (engine: [kstein78/selo](https://github.com/kstein78/selo), submodule in `themes/selo`).
Editor: Svetlana Morozova. Co-founder and developer: Konstantin Stein.
Languages: Serbian (Latin + Cyrillic), Croatian, English, Russian; German and Hungarian ready in `hugo.toml`
(`disableLanguages`) once translated.

## Work on the site

```
git clone --recurse-submodules https://github.com/kstein78/vajska.rs
cd vajska.rs
python3 themes/selo/scripts/sr_cyrl.py          # Serbian Cyrillic from content/sr
hugo server                                     # http://localhost:1313/
hugo --gc --minify && python3 themes/selo/scripts/seo_check.py public
```

Engine update: `git submodule update --remote themes/selo && git commit -am "Engine update"`.

Preview: GitHub Pages (noindex), https://kstein78.github.io/vajska.rs/ after Settings -> Pages -> Source: GitHub Actions.

## Launch checklist

1. DNS of vajska.rs: A record to the Hetzner server (same as rakovac.rs); add the site to the server (Caddy site block,
   clone with submodules, update timer), like deploy/ in rakovac.rs.
2. Google Search Console: add a **Domain property** for vajska.rs, verify with the TXT record at the registrar,
   submit https://vajska.rs/sitemap.xml. Discover traffic shows under Performance -> Discover once there is enough of it.
3. Bing Webmaster Tools: import from Search Console. Yandex Webmaster: add the site.
4. Remove the `{{< todo >}}` notes from the home pages, replace illustrations with real photos (data/photos.yaml).
