# rubocop-config
Central rubocop config to be shared among Rails applications

## Installation

Add this line to your application's .rubocop.yml:

```yaml
  inherit_from:
    # use the most up-to-date version of this config
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.yml
```

For new apps you can use this template:
```yaml
---
require:
  # add the corresponding gems to your Gemfile!
  - rubocop-rails
  - rubocop-performance
  - rubocop-minitest

inherit_from:
  # use the most up-to-date version of this config
  - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.yml

```

There are configs available for different types of projects. You can use them by adding the corresponding line to your .rubocop.yml.
Each combination of ruby and rails versions has its own tag in the repository and can be used by the following lines.

### Ruby 3 and Rails 7

```yaml
  inherit_from:
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/ruby3-rails7/.rubocop.yml
```