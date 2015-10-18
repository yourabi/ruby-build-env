# ruby-build-env
Vagrant/Ansible environment to build ruby debs for Debian/Ubuntu hosts. ruby-build-env uses [ruby-install](https://github.com/postmodern/ruby-install) and [fpm](https://github.com/jordansissel/fpm)

[issues]: https://github.com/yourabi/ruby-build-env/issues
[new-issue]: https://github.com/yourabi/ruby-build-env/issues/new

A build.yml is required. You can build debs for multiple Ruby implements (MRI, JRuby...etc) and multiple versions in one run.

A simple build.yml might look something like this

```yaml
---
rubies:
  - type: ruby
    versions:
    - version: 2.2.3
```

A slightly more complicated example might look something like this.

```yaml
---
rubies:
  - type: ruby
    versions:
    - version: 1.9.3
    - version: 2.2.3
  - type: jruby
    versions:
    - version: 9.0.1.0
```
