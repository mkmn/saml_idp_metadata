# SAML IdP Metadata Parser
[ ![](https://img.shields.io/gem/v/saml_idp_metadata.svg)](https://rubygems.org/gems/saml_idp_metadata) [ ![](https://img.shields.io/gem/dt/saml_idp_metadata.svg)](https://rubygems.org/gems/saml_idp_metadata)
[![CircleCI](https://circleci.com/gh/tknzk/saml_idp_metadata.svg?style=svg)](https://circleci.com/gh/tknzk/saml_idp_metadata)

Parser for SAML IdP metadata

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'saml_idp_metadata'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install saml_idp_metadata

## Usage

Basic one:

```ruby
# validate_xmlsn

xml = File.read('./idp_metadata.xml')

SamlIdpMetadata::Parser.call(xml: xml).validate_xmlns
```

```ruby
# ensure_params?
xml = File.read('./idp_metadata.xml')

SamlIdpMetadata::Parser.call(xml: xml).ensure_params?
```

```ruby
# build_params
xml = File.read('./idp_metadata.xml')

SamlIdpMetadata::Parser.call(xml: xml).build_params
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/tknzk/saml_idp_metadata. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Code of Conduct

Everyone interacting in the SamlIdpMetadata project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/tknzk/saml_idp_metadata/blob/master/CODE_OF_CONDUCT.md).
