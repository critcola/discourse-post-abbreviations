<a href="https://critcola.com/?utm_source=github.com&utm_medium=readme&utm_term=logo&utm_content=discourse-post-abbreviations&utm_campaign=development">![Logo](https://critcola.com/assets/images/crit-cola-banner.svg)</a>

# Discourse Post Abbreviations

This plugin for Discourse, customized for Crit Cola, wraps `<abbr>` HTML tags around a curated list of well known acronyms and abbreviations in posts, improving UX and SEO.

## Demo

See it in action and test it out for yourself on [Crit Cola's Discourse](https://critcola.com/community/?utm_source=github.com&utm_medium=readme&utm_term=demo&utm_content=discourse-post-abbreviations&utm_campaign=development).

## Installation

Add the plugin's repository URL to your container's `app.yml` file, for example:

```yml
hooks:
  after_code:
    - exec:
        cd: $home/plugins
        cmd:
          - mkdir -p plugins
          - git clone https://github.com/critcola/discourse-post-abbreviations.git
```

Rebuild the container:

```
cd /var/discourse
./launcher rebuild app
```

For the plugin to apply retroactively, you'll need to rebake old posts:

```
cd /var/discourse
./launcher enter app
rake posts:rebake
```

## About Crit Cola

Crit Cola is connecting and empowering the world's best players. Primarily an [Overwatch clan](https://critcola.com/?utm_source=github.com&utm_medium=readme&utm_term=overwatch-clan&utm_content=discourse-post-abbreviations&utm_campaign=development), we're a growing community of PC gamers. Join our [Steam group](http://steamcommunity.com/groups/critcola) and follow us on [Twitter](https://twitter.com/CritColaGaming). Cheers!

## License

The Discourse Post Abbreviations plugin is released under the [MIT License](LICENSE).
