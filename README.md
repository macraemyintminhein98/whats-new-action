# What's New GitHub Action

Automate your project's `README.md` changelog!

The What's New GitHub Action automatically generates a 'What's New' section based on your recent merged pull requests. Keep your users informed and your documentation fresh without manual updates.

## Features

*   **Automated Changelog:** Fetches merge PRs and formats them.
*   **Customizable:** Configure section title and history depth.
*   **Easy Setup:** Integrate in minutes into your existing workflow.

## Usage

Add this to your workflow:

yaml
name: Update What's New
on:
  push:
    branches:
      - main
jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: apex-product-builds/whats-new-action@v1
        with:
          # Optional: token for private repos or higher limits
          github_token: ${{ secrets.GITHUB_TOKEN }}
          # Optional: section title (default: "What's New")
          section_title: "Recent Changes"
          # Optional: days to look back (default: 30)
          days_limit: 60


## Pricing

Free for one repository. Upgrade for additional repository integrations via our website.

[Install on GitHub Marketplace](https://github.com/apps/whats-new-action)