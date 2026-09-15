# Xuehai Huang — Academic Homepage

Source for [xuehaihuang.github.io](https://xuehaihuang.github.io), built with GitHub Pages and Jekyll.

## Updating publications

Edit `_data/publications.yml`. Each record supports:

- `title`, `authors`, `journal`, `volume`, `pages`, and `year`
- `status` (for example, Published or Preprint)
- `doi`, `arxiv`, or `url`
- `selected: true` to feature the paper on the homepage

Keep records in reverse chronological order. Formal bibliographic details should be checked against journal records and MathSciNet.

## Updating news

Edit `_data/news.yml`. The homepage displays each dated item in file order.

## Local preview

If Jekyll is installed, run:

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://127.0.0.1:4000`.
