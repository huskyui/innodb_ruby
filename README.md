# A parser for InnoDB file formats, in Ruby

[![rspec test status](https://github.com/jeremycole/innodb_ruby/actions/workflows/rspec.yml/badge.svg)](https://github.com/jeremycole/innodb_ruby/actions/workflows/rspec.yml)
[![rubocop style check status](https://github.com/jeremycole/innodb_ruby/actions/workflows/rubocop.yml/badge.svg)](https://github.com/jeremycole/innodb_ruby/actions/workflows/rubocop.yml)

The purpose for this library and tools is to expose some otherwise hidden internals of InnoDB. This code is not intended for critical production usage. It is definitely buggy, and it may be dangerous. Neither its internal APIs or its output are considered stable and are subject to change at any time.

It is intended as for a few purposes:

* *As a learning tool.* What better way to improve your understanding of a structure than to implement it in another language?
* *As a teaching tool.* Using `irb` to interactively investigate the actual structures on disk is invaluable for demonstrating (to yourself or others) what is actually happening.
* *As an investigative tool.* InnoDB unfortunately doesn't provide enough information about what it is doing or has done with its on-disk storage. How full are pages? Exactly how many records per page? How is the B+tree structured for a particular table? All of these questions can be answered easily with `innodb_ruby`.
* *As a debugging tool.* While making changes to the structures or behaviors of InnoDB, it is necessary to have tools to expose the results both of the original behavior and the new one, in order to validate that the changes have the desired effect.

Various parts of this library and the tools included may have wildly differing maturity levels, as it is worked on primarily based on immediate needs of the authors.

# Resources

* The [innodb_ruby wiki](https://github.com/jeremycole/innodb_ruby/wiki) contains some additional references and documentation to help you get started.
* See the [RubyGems page for innodb_ruby](http://rubygems.org/gems/innodb_ruby) &mdash; Gem packaged releases are published regularly to RubyGems.org, which also provides online documentation.

# docker
* require `docker version` greater than `20.10.6`

```
cd middleware-compose
docker-compose up -d

docker ps 

docker exec -it xxxx /bin/sh

```