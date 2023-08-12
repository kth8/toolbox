Ansible playbook to install some CLI tools in a new Fedora [Toolbox](https://containertoolbx.org/) container. Packages from the fedora repo as defined in [config.yml](./config.yml) and others including:

https://github.com/aandrew-me/tgpt

https://github.com/Umio-Yasuno/amdgpu_top

https://github.com/71/lesspass.rs

https://github.com/magic-wormhole/magic-wormhole.rs

https://github.com/1player/host-spawn

Also create symlinks to host CLI utilities using `host-spawn`.

```shell
toolbox enter -y
git clone https://github.com/kth8/toolbox.git
sudo dnf install --repo fedora --assumeyes ansible
ansible-playbook toolbox/main.yml
```
