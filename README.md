# wheaties-brain

wheaties-brain combines [Brane](https://github.com/raws/brane-memory) and [Cinch](https://rubygems.org/gems/cinch) into a simple Markov chat bot. The brain is stored in memory, so it only exists for the lifetime of the process.

## Usage

wheaties-brain requires Ruby ≥ 2.0. Use [Bundler](https://bundler.io) to install dependencies.

```sh
gem install bundler
bundle install
```

Create a JSON configuration file.

```json
{
  "channels": ["#foo"],
  "nick": "Wheaties",
  "password": "s3cr3t",
  "port": 6667,
  "real": "wheaties@example.com",
  "server": "irc.example.com",
  "use_ssl": true,
  "verify_ssl": true,
  "user": "wheaties"
}
```

Run `bin/wheaties-brain` with the path to your configuration file.

```sh
bin/wheaties-brain path/to/config.json
```

## License

MIT
