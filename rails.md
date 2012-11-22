Rails notes
===========

## Sweet gems

 * [bootstrap-sass](https://github.com/thomas-mcdonald/bootstrap-sass)
 * [google-search](https://github.com/visionmedia/google-search)

## Recommended (Haven't tried)

 * [active_scaffold](https://github.com/activescaffold/active_scaffold/)

## ActiveRecord types

    :string
    :text
    :integer 
    :float
    :decimal
    :datetime
    :timestamp
    :time
    :date
    :binary
    :boolean

## Not serve static assets on development mode

Add to `config/environments/development.rb`:

    # Do not serve compiled assets
    config.serve_static_assets = false
