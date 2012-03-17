# Seajure

The web site for the Seattle Clojure Group.

## Usage

    $ lein run

This will place output HTML in the public/ directory.

## Swarming

Also contains a few files for setting up swarm coding sessions in the
`swarming/` directory. There's an `id_swarm` keypair as well as a
`swarmup.sh` script to set up a fresh user account for swarm coding.

    $ sudo adduser swarm --gecos "" # set password to swarm
    $ sudo -u swarm -i
    $ wget git.io/swarmup.sh
    $ sh swarmup.sh

## License

Copyright © 2010-2012 the Seattle Clojure Group
Released under the Eclipse Public License.
