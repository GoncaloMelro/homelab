# homelab
this is the repo for my home lab

# intro
i wanted to create a home lab to try some thing, learn and use some utilities
currently using a old laptop with a broken keyboard (8GB RAM and 500GB SSD Disk)
installed the lastest ubuntu server with my settings with no lvm group


# what was done
for now i just installed docker and immich and made some configs that i needed on the system, like avoid suspend when i close the lid of my laptop
configured an ssh connection
dhcp to ensure a static ip for my server, if we can call him that
installed docker
setup immich

# ansible
really wanted to use ansible to get stated on infra as code. and migth be usefull a later setup and self documenting

## pre requisites
    sudo apt update
    sudo apt install ansible -y
    sudo apt install sshpass -y

## commands
    ansible-playbook -i inventory.ini setup-server.yml --check --diff --ask-become-pass


# want i want to do later
configure pihole, for fun
create a web server with a custom dashboard for personal use
expose the server, with a vpn (currently running just local)
explore some cool docker images
configure a reverse proxy
i would like to turn on the server via ethernet, so i can save energy, if that was possible that would be fun to do
