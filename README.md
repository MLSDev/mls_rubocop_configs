# 👋

## Info

Check out this guys for more details about RuboCop [configuration](https://rubocop.readthedocs.io/en/latest/configuration).

## HOW TO

The example of `.rubocop.yml` file, the we consider to use:

```yml
require: rubocop-rspec
require: rubocop-performance

ingerit_from:
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/vX.X.X/.rubocop_general.yml
  - https://raw.githubusercontent.com/MLSDev/mls_rubocop_configs/vX.X.X/.rubocop_rspec.yml

AllCops:
  TargetRubyVersion:  RUBY.VERSION # keep me up-to-date
  TargetRailsVersion: RAILS.VERSION # keep me up-to-date
  Exclude:
    - 'db/**/*'
    - 'lib/apidocs/**/*'

```

Dont forget to keep UR `RUBY.VERSION` and `RAILS.VERSION` up-to-date while updating the rubocop.

## The things U should know

`RuboCop` got used to update their configs so often, please, report any issue U faced with. 

## About MLSDev

![MLSdev][logo]

The repo is maintained by MLSDev, Inc. We specialize in providing all-in-one solution in mobile and web development. Our team follows Lean principles and works according to agile methodologies to deliver the best results reducing the budget for development and its timeline.

Find out more [here][mlsdev] and don't hesitate to [contact us][contact]!

[mlsdev]:  https://mlsdev.com
[contact]: https://mlsdev.com/contact_us
[logo]:    https://raw.githubusercontent.com/MLSDev/development-standards/master/mlsdev-logo.png "Mlsdev"
