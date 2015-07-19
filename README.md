# oh-my-zsh

This is an [ansible](http://www.ansible.com) role which: 

  * installs zsh
  * installs oh-my-zsh

Configuration of oh-my-zsh is eschewed in favour of better config management tools like dotfiles.

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install glennr.oh-my-zsh
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install glennr.oh-my-zsh
```

Using `git`:

```
$ git clone https://github.com/glennr/glennr.oh-my-zsh.git
```

## Dependencies

This role requires you to have `git` installed.

## Variables

Not much here. Unlike many other playbooks, this one is intentionally simple, leaving out any oh-my-zsh related configuration. It installs a very simple default .zshrc into $HOME. Further configuration should happen with something like dotfiles.

If you are installing on Debian/Ubuntu, you'll need to set a target user in {{ user }}. On OSX it will just default to the ansible user.

## Example Playbook (OSX)

    - hosts: servers
      roles:
         - glennr.oh-my-zsh

(installs just for the ansible user)

## Example Playbook (Debian/Ubuntu)

    - hosts: servers
      vars:
         user: alex
      roles:
         - glennr.oh-my-zsh


## License

LGPL

## Author Info

Glenn Roberts, g@glenn-roberts.com

## Credits 

Alex Lourie, djay.il@gmail.com

Jasper N. Brouwer, jasper@nerdsweide.nl

Ramon de la Fuente, ramon@delafuente.nl
