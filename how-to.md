
  866  git clone ssh://git@github/duncombe/sos-guidelines.git
  867  cd sos-guidelines/
  871  git remote add upstream ssh://git@github/ioos/sos-guidelines.git
  872  git fetch upstream
  909  git remote -v
  910  git fetch --all
  911  git log --oneline --graph



 1135  hugo server  --buildDrafts 

 1151  git push ssh//git@github/duncombe/test-site alex-master:master
 1152  git push ssh://git@github/duncombe/test-site alex-master:master

 1161  git checkout --orphan test-gh-pages
 
 1163  git rm --cached $(git ls-files)

 1168  git push ssh://git@github/duncombe/test-site test-gh-pages:gh-pages
 1169  git checkout alex-master


 1173  git checkout -f alex-master
 1175  rm -rf public/
 1176  git subtree add --prefix public ssh://git@github/duncombe/test-site test-gh-pages:gh-pages --squash
 1177  git status
 1178  git add -A
 1179  git commit -m "fixing the problems"

 1184  git subtree add --prefix public ssh://git@github/duncombe/test-site gh-pages --squash
 1185  git subtree add --prefix public ssh://git@github/duncombe/test-site test-gh-pages --squash
 1186  git status
 1187  git checkout test-gh-pages
 1188  git status
 1189  git rm --cached $(git ls-files)
 1190  git status
 1191  git add README.md 
 1192  git commit -m "INIT: initial commit on gh-pages branch"
 1193  git checkout alex-master README.md
 1194  git add README.md 
 1195  git checkout alex-master README.md
 1196  git commit -m "INIT: initial commit on gh-pages branch"
 1197  git push ssh://git@github/duncombe/test-site test-gh-pages
 1198  git push -f ssh://git@github/duncombe/test-site test-gh-pages
 1199  git checkout alex-master
 1200  ls -altr
 1201  rm -rf public
 1202  ls
 1203  vi chris-notes.md 
 1204  git remote -v
 1205  git fetch --all
 1206  git status
 1207  git help merge abirger
 1208  git merge abirger/master
 1209  git status
 1210  vi .gitignore 
 1211  git status
 1212  git add -A
 1213  git status
 1214  git commit -m "Adding the files we need to make the web-site."
 1215  git merge abirger/master
 1216  git status
 1217  vi .gitignore
 1218  vim config.toml 
 1219  vim layouts/chrome/sidebar.html
 1220  ls images
 1221  ls -altr
 1222  vim layouts/chrome/sidebar.html
 1223  find . -iname images -print
 1224  vim layouts/chrome/sidebar.html
 1225  find . -iname "ioos*" -print
 1226  xv ./static/images/ioos_blue2.png
 1227  xv ./doc/wsdd/images/ioos_blue2.png
 1228  diff ./doc/wsdd/images/ioos_blue2.png ./static/images/ioos_blue2.png
 1229  ls -ltr
 1230  status
 1231  git status
 1232  history -10
 1233  history 10
 1234  history 20
 1235  git status
 1236  git add .gitignore config.toml  layouts/chrome/sidebar.html 
 1237  vim layouts/index.html
 1238  vi layouts/index.html
 1239  vim layouts/index.html
 1240  git add layouts/index.html
 1241  git status
 1242  git help merge 
 1243  git commit 
 1244  ls -ltr
 1245  vi README.md 
 1246  history > how-to.md
