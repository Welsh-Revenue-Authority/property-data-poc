# Property data proof of concept site

The team site for the [land and property data proof of concept](https://welsh-revenue-authority.github.io/property-data-poc/en/) site by the [WRA](https://gov.wales/welsh-revenue-authority).

## Getting started

The site is hosted on github pages. The instructions below are for running the site locally.

### Dependencies

* Ruby
* Bundler

### Running locally

Install required gems
```
bundle install
```

Run the site with
```
bundle exec jekyll serve
```

### Developing it locally

The frontend assets require Node.

If you are working on the site locally you should install the dev-dependencies. Run
```
npm install
```

Work on the `.scss` file in `/src/scss`.

When ready to compile your stylesheet(s) run
```
npm run build:stylesheets
```

Or, alternatively, to compile them whilst you are working run the watch command.
```
npm run watch
```

## Making it bilingual

Using this jekyll plugin allows us to make sure the site is bilingual.

https://juan.pallares.me/configure-jekyll-multi-language-without-plugin/
