# oh-my-zsh

Installs zsh and oh-my-zsh

Unlike many other playbooks, this one is intentionally simple, leaving out any oh-my-zsh related configuration. It installs a very simple default .zshrc into $HOME. Further configuration should happen with something like dotfiles.

## Example Playbook (OSX)

    - hosts: servers
      roles:
         - glennr.oh-my-zsh

(installs to ansible user)

## Example Playbook (Debian/Ubuntu)

    - hosts: servers
      vars:
         user: alex
      roles:
         - glennr.oh-my-zsh

License
-------

LGPL

Author Information
------------------

Glenn Roberts, g@glenn-roberts.com

Based on bash work by:
------------------

Alex Lourie, djay.il@gmail.com

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
