# Spam Filters

Cold email spam is an Inbox menace. Kill them with :fire:.

This utility is a list of domains that generates rules for GMail. Since GMail has a limit of 1024 characters per filter, the rules are broken up into segments. 


## Usage

```bash
$ ./build
---
Built 3 rules with 186 domains.

```
The file `rules.yaml` will have an array of strings that you can use to create & maintain the filters.

### Add a new rule to GMail

- Visit the [Filters and Blocked Addresses](https://mail.google.com/mail/u/0/#settings/filters) in GMail
  - This link assumes the first GMail account you're logged into
- Scroll down to "Create a New Filter"
- Paste one of the rules from `rules.yaml` into the `from` field
- Click `Create Filter`
- Check the boxes for: 
  - `Skip Inbox (Archive It)`, 
  - `Apply the Label` and pick a new label so you don't lose these
  - `Also apply filter to matching conversations.`
- Click `Save Filter`

### Update an existing rule in GMail

- Visit the [Filters and Blocked Addresses](https://mail.google.com/mail/u/0/#settings/filters) in GMail
    - This link assumes the first GMail account you're logged into
- Pick your most recent filter
- Paste the last rule from `rules.yaml` into the `from` field
- Click `Continue`
- Ensure these boxes are checked:
    - `Skip Inbox (Archive It)`,
    - `Apply the Label` and pick your cold spam label
    - `Also apply filter to matching conversations.`
- Click `Update Filter`

## Notes

- Domains will be unique, so don't be afraid to add dupes

## Contributing

- Add a domain to `data/domains.yaml`
- Build your rules in the terminal
- Contribute back to the repo
