# 👋

## Info

Check out this guys for more details about RuboCop [configuration](https://rubocop.readthedocs.io/en/latest/configuration).

## HOW TO

The example of `.rubocop.yml` file, the we consider to use:

```yml
require:
  - rubocop/cop/internal_affairs
  - rubocop-performance
  - rubocop-rspec
  - rubocop-thread_safety
  - rubocop-i18n

inherit_from:
  - .rubocop_todo.yml # optional
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/vX.X.X/.rubocop_general.yml
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/vX.X.X/.rubocop_rspec.yml

AllCops:
  TargetRubyVersion:  RUBY.VERSION # keep me up-to-date
  TargetRailsVersion: RAILS.VERSION # keep me up-to-date
  Exclude:
    - 'db/**/*'
    - 'lib/apidocs/**/*'
    - 'bin/**/*'

```

Dont forget to keep UR `RUBY.VERSION` and `RAILS.VERSION` up-to-date while updating the rubocop.

`vX.X.X` in config links suppose to be version of configs to use latest stable one. Or if U'r brave enough - U can use it directly from `master` branch like 

```yml
inherit_from:
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/master/.rubocop_general.yml
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/master/.rubocop_rspec.yml
```

If dont want to keep downloads in your project, just add: 

```bash
.rubocop-https*
```

to `.gitignore` file.

## The things U should know

`RuboCop` got used to update their configs so often, please, report any issue U faced with. 

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## About MLSDev

![MLSdev][logo]

The repo is maintained by MLSDev, Inc. We specialize in providing all-in-one solution in mobile and web development. Our team follows Lean principles and works according to agile methodologies to deliver the best results reducing the budget for development and its timeline.

Find out more [here][mlsdev] and don't hesitate to [contact us][contact]!

[mlsdev]:  https://mlsdev.com
[contact]: https://mlsdev.com/contact_us
[logo]:    https://raw.githubusercontent.com/MLSDev/development-standards/master/mlsdev-logo.png "Mlsdev"
