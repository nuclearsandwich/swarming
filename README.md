# Swarming

A set of scripts and dotfiles to bootstrap swarm coding.

## Usage

***NOTE:*** Only the host of the swarming session needs to follow the
instructions below.

### Participating Prerequisites

- A \*nix terminal. If you're on Windows, check out the [PuTTY][] program.
- Basic familiarity or affinity to a terminal-based editor such as [Emacs][] or
  [Vim][]
- Someone willing to host a swarm coding session.

Connect to a swarm host
with the following commands\*.

    $ ssh swarm@$HOST_IP
    $ tmux attach swarming

\* With PuTTY, you will actually be entering the host ip in a Windows dialogue,
then prompted for the username later.

### Hosting Prerequisites

#### Permissions

1. Be on a \*nix machine
2. Have the ability to sudo

#### Software

- [sshd][]
- [tmux][]
- A terminal-based $EDITOR of your choice, [Vim][] and [Emacs][] are currently
  supported.

### Pre-installation

<ul>
  <li>Add a user with username swarm to your machine.
  <p> Suggested command: <code><pre>$ sudo adduser swarm --gecos "" # set password to swarm</pre></code></p>
  </li>
  <li>Start your ssh daemon after ensuring swarm is accessible via ssh.</li>
  <li>Start an interactive shell as swarm.
  <p><code><pre>$ sudo -u swarm -i</pre></code></p>
  </li>
</ul>

### Installation 
*As the User* __swarm__
    $ git clone git://github.com/nuclearsandwich/swarming.git
    $ swarming/$EDITOR/swarm.sh

### Go Swarm!

After bootstrapping [leiningen][] and symlinking the appropriate dotfiles for
your chosen $EDITOR, the last command will start a tmux session called
`swarming` as well as print a message that you can share with your swarm on how
to connect.

    ==> Created tmux session
    ==> Bootstrapping Leiningen
    ==> Symlinking Editor Dotfiles
    ==> Direct the swarm to connect using $ ssh swarm@10.10.10.7
    ==> Happy Swarming

## Roadmap

The dependency on the root sshd server is both a security risk to host machine
and a pain point for flexible, yet precise instructions. It'd be cool to bundle
an embedded ssh daemon (Dropbear?) and run it as the non-privileged swarm user
on port 5022 or something.

Since Swarm coding is not, as a rule, bound to Clojure just as it was not bound
to emacs, I would like to add support for other languages such as Ruby, Python,
Go, or Racket.

## License

Copyright © 2010-2012 the Seattle Clojure Group
Released under the Eclipse Public License.

[PuTTY]: 
[Vim]: 
[Emacs]: 
[leiningen]: 
[tmux]: 
[sshd]: 
