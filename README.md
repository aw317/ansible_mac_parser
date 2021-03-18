### Preapration:

Install ansible:

```
sudo apt-get install software-properties-common
sudo apt-add-repository --yes --update ppa:ansible/ansible

sudo apt-get install ansible

```

### Usage
To run on localhost:
```
ansible-playbook gey_company_name.yml -i inventories/local/ -e mac_address="44:38:39:ff:ef:57" --ask-vault-pass

```
And in output you should see somethink like:

```
TASK [get_company_name : debug] *************************************************************************************************************************************************************
ok: [localhost] => {
    "msg": "Cumulus Networks, Inc"
}
```
where "Cumulus Networks, Inc" is returned vendor 