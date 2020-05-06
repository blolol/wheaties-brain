# wheaties-brain

wheaties-brain combines [Brane](https://github.com/raws/brane-memory) and [Cinch](https://rubygems.org/gems/cinch) into a simple Markov chat bot that learns from chatter in IRC channels, and responds whenever the bot's nickname is mentioned. The brain is stored in memory, so it only exists for the lifetime of the process.

## Usage

wheaties-brain requires Ruby ≥ 2.0. Use [Bundler](https://bundler.io) to install dependencies.

```sh
gem install bundler
bundle install
```

Create a JSON configuration file. You can copy `config.example.json` as a starting point.

| Key | Required? | Description |
|-----|-----------|-------------|
| `channels` | **Required** | An array of IRC channels to join. |
| `learn` | Optional | An array of file paths to load into the bot's brain before connecting to the IRC server. Each file should contain one sentence per line. Each path will be expanded using Ruby's [File.expand_path](http://ruby-doc.org/core-2.7.1/File.html#method-c-expand_path). |
| `messages_per_second` | Optional | Max messages per second to send. Default: 100. |
| `nick` | **Required** | The bot's nickname. |
| `password` | Optional | The server password. |
| `port` | **Required** | The server port. |
| `real` | **Required** | The bot's real name. |
| `server` | **Required** | The server address. |
| `use_ssl` | Optional | `true` enables TLS/SSL. Default: `false`. |
| `user` | **Required** | The bot's username. |
| `verify_ssl` | Optional | `true` enables TLS certificate verification. Default: `false`. |

Run `bin/wheaties-brain` with the path to your configuration file as a command line argument.

```sh
bin/wheaties-brain path/to/config.json
```

## License

MIT
