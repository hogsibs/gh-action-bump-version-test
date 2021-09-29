# Test Details
## .github/workflows/push.yml
```YAML
name: Bump Version (Custom Tag Prefix)
'on':
  push: null
jobs:
  bump-version:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - id: version-bump
        uses: ./action
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          tag-prefix: v

```
## Message
no keywords
## Starting Version
18.0.0
## Expectation
- **Version:** 18.0.1
- **Tag:** v18.0.1