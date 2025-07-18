# Gym-Git-Exercise-Solutions
# Bundel1- exercise 2
``` bash
   user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (dev)
$ touch home.html
  user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (dev)
$ touch about.html
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (dev)
$ touch team.html 


```
## bundel 2 - exercise 1:
``` bash
 I created new branch below:
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (dev)
$ git branch ft/bundle-2 

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/bundle-2)
$ touch service.html


```
## Bundle 2 - exercise 2:
```
// I already made pull from origin main the latest changes

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (main)
$ git branch ft/service-redesign

// all changes I made in service.html 
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (main)
$ git push origin main
// now I'm going to ft/service-redesign




```
# Bundle 1
# Exercise 1: here I delete files and folder  are not neccessary to my project all  now are done/

```bash 
 $ git rm -r git-files
rm 'git-files/about.html'
rm 'git-files/home.html'

```
## Bundle 2
### bundle 3 exercise 1:
```
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/team-page)  
$ touch team.html

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (main)
$ git branch ft/contact-page
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/contact-page)
$ git switch ft/team-page
Switched to branch 'ft/team-page'

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/team-page)  
$ git log
commit 2d50f4915b8d04b512758373b8eaf39ecb9a5c1a (HEAD -> ft/team-page, origin/ft/team-page)
Author: system sylvere BARINDA <systembarinda@gmail.com>
Date:   Fri Jul 18 11:58:18 2025 +0200

    in team files are added some new changes


user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/contact-page)
$ git log ft/team-page -1 
commit 2d50f4915b8d04b512758373b8eaf39ecb9a5c1a (origin/ft/team-page, ft/team-page)
Author: system sylvere BARINDA <systembarinda@gmail.com>
Date:   Fri Jul 18 11:58:18 2025 +0200

    in team files are added some new changes



user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/contact-page)
$ touch contact.html    

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/faq-page)
$ touch faq.html

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/faq-page)   
$ git revert ft/team-page
[ft/faq-page 2595d65] Revert "in team files are added some new changes"
 1 file changed, 4 deletions(-)


user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/faq-page)   
$ git add .

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/faq-page)   
$ git commit -m"  I just made new revert in this branch"
[ft/faq-page 60b7d87]   I just made new revert in this branch
 1 file changed, 5 insertions(+)

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/faq-page)   
$ git push origin ft/faq-page



```
### bundle 3 exercise

``` bash 

user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (main)
$ git switch ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
Your branch is up to date with 'origin/ft/home-page-redesign'.
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/home-page-redesign)
$ git fetch origin
user@LAPTOP-ICNU96T9 MINGW64 ~/Documents/GitHub/Gym-git-Exercise-Solutions (ft/home-page-redesign)
$ git rebase main


```
