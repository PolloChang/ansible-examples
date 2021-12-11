# ansible-examples
ansible 範例

## 開發方式

* vagrant

### vagrant 安裝

* vagrant

安裝完成後可能需要重新開機

以下為安裝方式

```sehll
curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
# sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
sudo apt-get update && sudo apt-get install vagrant
vagrant version
```

* plugin

```bash
vagrant plugin install vagrant-libvirt
vagrant plugin install vagrant-mutate
vagrant plugin install sahara
```

* ansible-lint 

https://github.com/ansible-community/ansible-lint

```
sudo apt install ansible-lint
ansible-lint --version
```

### vagrant 相關使用

* 新增 box

```bash
 vagrant box add bento/debian-8.6 https://atlas.hashicorp.com/bento/boxes/debian-8.6
```

* 檢查一下目前所有安裝在本機的 Vagrant boxes

```bash
vagrant box list
```

* 移除不再需要的 box

```bash
vagrant box remove bento/debian-8.6
```

* 確認當前 Vagrant 主機的運作狀況

```bash
vagrant status
```

* 列出主機的相關資訊

```bash
vagrant ssh-config

Host centOS6
  HostName 192.168.121.2
  User vagrant
  Port 22
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile /home/jameschang/Documents/vagrant/workspace/.vagrant/machines/centOS6/libvirt/private_key
  IdentitiesOnly yes
  LogLevel FATAL
```

* 休眠
  
```bash
vagrant spend
```

* 關機

```bash
vagrant halt
```

* 刪除

```bash
vagrant destroy --force
```

### Vagrantfile 

* 指定主機名稱

config.vm.define "serverName"


## 學習相關資源

[在地端建置Angular+ASP.NET Core的DevOps環境](https://ithelp.ithome.com.tw/users/20107868/ironman/1621)

* Vagrant

[Vagrant Cloud](https://app.vagrantup.com/boxes/search)

[Vagrant 筆記](https://blog.codylab.com/vagrant/)

[Ubuntu 上 Vagrant+Libvirt 虛擬環境](https://samkuo.me/post/2020/06/vagrant-libvirt-ubuntu-devops-env/)

* Ansible

[ansible中文權威指南](https://chusiang.github.io/ansible-docs-translate/intro.html)

[怎麼安裝 Ansible](https://ansible.tw/#!docs/installation.md)
(https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-debian)

[Download Vagrant](https://www.vagrantup.com/downloads)

[Ansible.Builtin{對應linux 指令}](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/)

[ansible.builtin.apt](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html)

[Ansible Documentation](https://docs.ansible.com/ansible/latest/index.html)

* Playbook

[Playbook Keywords](https://docs.ansible.com/ansible/latest/reference_appendices/playbooks_keywords.html)

* role

[官網找別人封裝好的role](https://galaxy.ansible.com/)
