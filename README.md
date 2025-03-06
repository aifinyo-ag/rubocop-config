# rubocop-config
Central rubocop config to be shared among Rails applications

## Installation

> [!NOTE]
> There is a new [AifinyoUtils](https://github.com/aifinyo-ag/aifinyo_utils) gem that will take care of the rubocop configuration. Please use that instead of directly using this repository.

### Gemfile

Add these Gems to your application's Gemfile into the group `development` and `test`:

```ruby
group :development, :test do
  # your other gems

  gem 'rubocop', require: false
  gem 'rubocop-minitest', require: false # for minitest
  gem 'rubocop-performance', require: false # for performance
  gem 'rubocop-rails', require: false # for Rails
end
```

### .rubocop.yml

> [!CAUTION]
> This config only works from rubocop version 1.72 and up so use `>= 1.72.0` as version constraint.

Add this line to your application's .rubocop.yml:

```yaml
  inherit_from:
    # use the most up-to-date version of this config
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.yml
```

This config relies on the automatic version detection of rubocop.

### .gitignore

Make sure you add the following line to your .gitignore file:

```
# ignore remote rubocop config - rubocop handles this itself
# see https://docs.rubocop.org/rubocop/configuration.html#inheriting-configuration-from-a-remote-url
.rubocop-https---raw-githubusercontent-com-aifinyo-ag-rubocop-config-main--rubocop-*
```

Using rubocop with a remote config will make sure that you always use the most up-to-date version of the config.
Rubocop will [automatically check for updates](https://docs.rubocop.org/rubocop/configuration.html#inheriting-configuration-from-a-remote-url) when you run it when:

- The file does not exist.
- The file has not been updated in the last 24 hours.
- The remote copy has a newer modification time than the local copy.

### Supported versions
#### Ruby 3 and Rails 7

```yaml
  inherit_from:
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.ruby3-rails7.yml
```

## Development
If you want to contribute to this project, you need to discuss the changes with the team first. After that, you can create a branch, update the config (or provide a new one) and create a pull request.
