# deploy myth box to digital ocean

    ansible-playbook -i deploy/hosts deploy/deploy_digitalocean_playbook.yml  --vault-password-file=conf/vault_pass.txt

wait for DNS to propagate with "nslookup mythologic.eschaton.quest"

- ansible-playbook -i deploy/hosts deploy/secure_playbook.yml
- ansible-playbook -i deploy/hosts deploy/playbook.yml

# run

- on server:
  - (update ~/.vnc/xstartup or click through errors)
  - vncserver -localhost -nevershared :1
- on local box:
  - ssh -L 59000:localhost:5901 -C -N -F local/ssh_config mythologic.eschaton.quest
  - vncviewer localhost::59000
  - (or just run the client on the server over X)
- on vnc client:
  - ~/myth_2/Myth2_64bit
- on server:
  - vncserver -kill :1

- cd ~/myth_2
- ./Myth2_64bit
- new game
- other
- ok
- host a game
- port 42424
- ok
- options
- choose level, type (body count deathmatch is vanilla)
- server is observer

# notes

owner of myth files must be redarmorboy
myth port must be 42424
