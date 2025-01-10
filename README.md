autumn's notes:
FOR LIVE WORK:
  powershell:
  $ cd .\vue1\
  $ npm run serve

UPLOAD WORK 2 GITHUB:
  git bash in project folder
  $ git add .
  $ git commit -m ""
  $ git push -u origin main

HOW 2 DEPLOY:
  powershell:
  $ cd .\vue1\
  $ npm run build
  close powershell!

  git bash in project folder:
  $ git add dist && git commit -m 'adding dist subtree'
  $ git subtree push --prefix dist origin gh-pages

  ctrl + f5 site for updates!