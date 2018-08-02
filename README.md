# Hipmost

Hipmost is a tool to migrate your Hipchat history to Mattermost, it
parses your hipchat export and generates a file to be imported on
Mattermost

## Installation

For now:

    $ gem install specific_install
    $ gem specific_install -l https://gitlab.orbitalimpact.com/gabrielrios/hipmost.git

Eventually, it might be this:

    $ gem install hipmost

## Usage

    Usage: hipmost [options] [command]

    Commands:

    public (AKA, room or rooms)
    Form: public [import|list] [rooms] - Import or list public Hipchat rooms

    [rooms] must be at least one pair composed by "Hipchat channel name" and "Mattermost team":"Mattermost channel"
    The Mattermost team or channel can be the URL endpoint, such as "town-square", or the channel name, such as "General"

    --------

    private (AKA, direct)
    Form: private [import|list]  - Import or list private chats

    --------

    Examples:
    $ hipmost room import "Orbital Impact" "Orbital Impact":"General"
    $ hipmost public import "Orbital Impact" "Orbital Impact":"General" -p data_folder
    $ hipmost private list
    $ hipmost -v rooms import "Orbital Impact" "Orbital Impact":"General"

    -p, --path [PATH]     Path to Hipchat data folder (Default: "./data")
    -v, --[no-]verbose    Run verbosely

## Contributing

Bug reports and pull requests are welcome. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Ruby code of conduct.](https://www.ruby-lang.org/en/conduct/)

## License

The gem is available as open source under the terms of the [MIT License.](https://opensource.org/licenses/MIT)

## Code of Conduct

Everyone interacting in the Hipmost project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct.](https://www.ruby-lang.org/en/conduct/)
