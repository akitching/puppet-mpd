# Puppet MPD Module

Module for provisioning MPD (Music Playing Daemon)

Tested on Ubuntu 12.04, patches to support other operating systems are welcome.

## Installation

Clone this repo to your Puppet modules directory

    git clone git://github.com/ajjahn/puppet-mpd.git mpd

## Usage

Tweak and add the following to your site manifest:

    node 'server.example.com' {

      class {'mpd::client':
        volume => '100',
        repeat => 'on',
        random => 'off',
        single => 'off',
        consume => 'off',
        crossfade => '10',
        force_play => true,
        force_update => true,
        remove_duplicates => true,
      }

    }

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
