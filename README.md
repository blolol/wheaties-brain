# wheaties-brain

wheaties-brain combines [Brane](https://github.com/raws/brane-memory) and [Cinch](https://rubygems.org/gems/cinch) into a simple Markov chat bot.

## Usage

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

```
bin/wheaties-brain path/to/config.json
```

## License

MIT
