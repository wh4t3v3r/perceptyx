# Test

Simple set of ansible roles to deploy a PHP script, as requested via upwork.

### How to:
- Clone this repository and cd into it;
- Configure your target hostname in the 'hosts' file, by setting the ip address instead of 127.0.0.1 and configuring your username. The user should either be root or have sudo privileges;
- Run ansible playbooks as follows:
    ```sh
    $ ansible-playbook php.yml
    ```
    or, if you need to specify an ssh password:
    ```sh
    $ ansible-playbook --ask-pass php.yml
    ```
    or, specify an ssh key:
    ```sh
    $ ansible-playbook --private-key ~/.ssh/mykey.pem php.yml
    ```
    
    You can also customize what password to set for the mysql user:
    ```sh
    $ ansible-playbook php.yml --extra-vars "mysql_password=notasimplepw"
