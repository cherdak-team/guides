# Ruby

1. [Ruby Style Guide](https://github.com/rubocop-hq/rails-style-guide)

2. [Rails Style Guide](https://github.com/rubocop-hq/rails-style-guide)

3. [Rubocop](https://github.com/rubocop-hq/rubocop)

4. [Brakeman](https://github.com/presidentbeef/brakeman)

5. [Bundler Audit](https://github.com/rubysec/bundler-audit)

6. [Bullet](https://github.com/flyerhzm/bullet)

7. [Overcommit](https://github.com/brigade/overcommit)

8. [FFaker](https://github.com/ffaker/ffaker)

9. [Factory Bot](https://github.com/thoughtbot/factory_bot)

10. [RSpec](https://github.com/rspec/rspec-rails)

11. [Rubocop RSpec](https://github.com/rubocop-hq/rubocop-rspec)

### Rubocop Config

`.rubocop.yml`
```
require: rubocop-rspec

AllCops:
  TargetRailsVersion: 5.2
  DisplayCopNames: true
  DisplayStyleGuide: true

Rails:
  Enabled: true

Bundler/OrderedGems:
  Enabled: false

Layout/AlignParameters:
  EnforcedStyle: with_fixed_indentation

Layout/MultilineMethodCallIndentation:
  EnforcedStyle: indented

Layout/SpaceInLambdaLiteral:
  EnforcedStyle: require_space

Lint/AmbiguousBlockAssociation:
  Exclude:
    - "spec/**/*"

Metrics/AbcSize:
  Exclude:
    - "db/*.rb"
    - "db/migrate/*.rb"

Metrics/BlockLength:
  Exclude:
    - "config/routes.rb"
    - "config/initializers/*.rb"
    - "db/*.rb"
    - "db/migrate/*.rb"
    - "spec/factories/*.rb"

Metrics/LineLength:
  Max: 120
  Exclude:
    - "db/*.rb"

Metrics/MethodLength:
  Max: 20
  Exclude:
    - "db/migrate/*.rb"

Naming/VariableNumber:
  EnforcedStyle: snake_case

RSpec/ExpectChange:
  EnforcedStyle: block

RSpec/NestedGroups:
  Max: 4

Style/ClassAndModuleChildren:
  Enabled: false

Style/ConditionalAssignment:
  Enabled: false

Style/Documentation:
  Enabled: false

Style/NumericLiterals:
  Exclude:
    - "db/schema.rb"

Style/StringLiterals:
  EnforcedStyle: double_quotes

Style/SymbolArray:
  EnforcedStyle: brackets

Style/WordArray:
  EnforcedStyle: brackets
```
