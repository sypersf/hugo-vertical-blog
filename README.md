# Hugo Vertical Blog

PaperMod-based Hugo blog with **vertical Chinese writing (竖排)** and **page-flipping** navigation.

## Features

- Vertical text layout on desktop (writing-mode: vertical-rl)
- Page-flipping: long articles split into pages. Navigate via buttons, keyboard arrows, or touch swipe
- Portrait phones auto-switch to horizontal layout
- Works with existing PaperMod sites — just drop in the layouts

## Quick Start

```bash
# 1. Create Hugo site
hugo new site myblog && cd myblog

# 2. Install PaperMod
git init
git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod

# 3. Copy custom layouts from this repo
cp -r layouts/* myblog/layouts/

# 4. Edit hugo.toml
echo 'theme = "PaperMod"' >> hugo.toml

# 5. Run
hugo server -D
```

## How It Works

| File | Purpose |
|------|---------|
| `layouts/single.html` | Article template with page navigation controls |
| `layouts/_partials/extend_head.html` | CSS for vertical writing, responsive layout |
| `layouts/_partials/extend_footer.html` | JavaScript page-flipping engine |

Writing a post with 5+ chapters will trigger the multi-page flip experience.

## License

MIT
