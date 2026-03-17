# Johnny Hua's Engineering Notebook

This repository powers my personal blog at https://johnnyhua.github.io

## Structure

```
├── setup/          # Development environment
├── workflow/       # How I work with AI
├── problems/       # Pain points & challenges
├── solutions/      # How I solved problems
├── projects/       # Ideas & project status
└── assets/         # CSS, images, etc.
```

## Adding Content

### New Problem

1. Copy `problems/_template.md` to `problems/pXXX-short-name.md`
2. Copy `problems/_template-zh.md` to `problems/pXXX-short-name-zh.md`
3. Update `problems/index.md`

### New Solution

1. Copy `solutions/_template.md` to `solutions/sXXX-short-name.md`
2. Copy `solutions/_template-zh.md` to `solutions/sXXX-short-name-zh.md`
3. Update `solutions/index.md`

### New Project

1. Copy `projects/_template.md` to `projects/project-name.md`
2. Copy `projects/_template-zh.md` to `projects/project-name-zh.md`
3. Update `projects/index.md`

## Local Development

```bash
bundle install
bundle exec jekyll serve
```

## Deployment

Push to `main` branch. GitHub Pages will auto-deploy.