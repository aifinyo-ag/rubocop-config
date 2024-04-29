# rubocop-config
Central rubocop config to be shared among Rails applications

## Installation

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

Add this line to your application's .rubocop.yml:

```yaml
  inherit_from:
    # use the most up-to-date version of this config
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.ruby3-rails7.yml
```

There are configs available for different types of projects. You can use them by adding the corresponding line to your .rubocop.yml.
Each combination of ruby and rails versions that we use and support has its own file in the repository.

### Supported versions
#### Ruby 3 and Rails 7

```yaml
  inherit_from:
    - https://raw.githubusercontent.com/aifinyo-ag/rubocop-config/main/.rubocop.ruby3-rails7.yml
```

## Development
If you want to contribute to this project, you need to discuss the changes with the team first. After that, you can create a branch, update the config (or provide a new one) and create a pull request.
