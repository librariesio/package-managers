# Package Managers

Metadata extracted from [Libraries.io](https://libraries.io) about many different package managers in a standard format.

String interpolation of commands and urls is done using [mustache](https://mustache.github.io/) in an attempt at cross language compatibility.

All data is stored in JSON where the key for each package manager is the name of the repository in lower case.

Each attribute relates to the source of some information about a package that can be inferred from just the package manager, name of the package and optionally it's version.

See [`package-managers.json`](package-managers.json) for the full data set.

## Data format

```JSON
"rubygems": {
  "install": "gem install {{name}} {{#version}}-v {{version}}{{/version}}",
  "download": "https://rubygems.org/downloads/{{name}}-{{version}}.gem",
  "url": "https://rubygems.org/gems/{{name}}{{#version}}/versions/{{version}}{{/version}}",
  "documentation": "http://www.rubydoc.info/gems/{{name}}/{{version}}"
}
```

### Valid Keys

#### install

The shell command to install a package, possibly to install a specific version of that package.

#### download

The url to a tarball/zip of the source code of that package, most likely to a specific version of that package.

#### documentation

The url to automatically generated documentation for that package, possibly to a specific version of that package.

#### url

The url for the page on the repository website for that package, possibly to a specific version of that package.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/librariesio/package-managers. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.

## License

The project is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
