Summary of:
https://medium.freecodecamp.org/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca


# Multiple SSH Key GitHub Setup


## Clean SSH setup:


1) Generate default key for personal:


ssh-keygen -t rsa


2) Generate work Key:


ssh-keygen -t rsa -C "email@work_mail.com" -f "id_rsa_work_user1"


NOTE: This created the key on the root level and I had to manually move them to the SSH folder


3) Log into Personal GitHub Account


Copy Key: pbcopy < ~/.ssh/id_rsa.pub


GitHub>Settings>SSH & GPG Keys  New SSH Key  Name it   Paste


4) Log into Work Github


Copy Key: pbcopy < ~/.ssh/id_rsa_work_user1.pub


GitHub>Settings>SSH & GPG Keys  New SSH Key  Name it   Paste


5) Add to ssh-agent


eval "$(ssh-agent -s)"


ssh-add ~/.ssh/id_rsa

ssh-add ~/.ssh/id_rsa_work_user1

6) To Switch between the two keys:

            $ ssh-add -D            //removes all ssh entries from the ssh-agent
            $ ssh-add ~/.ssh/id_rsa    // adds personal

            $ ssh-add -D
            $ ssh-add ~/.ssh/id_rsa_work_user1 // adds work
            
     
