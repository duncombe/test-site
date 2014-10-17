sos-guidelines
==============

## Creating and updating sos-guidelines web-pages

1. Use Hugo to build your site.
	2.  Get and install Hugo from [gohugo.io](http://gohugo.io/overview/quickstart/), Step 1.  
	2. Following the quickstart Guide, have Hugo create a site    
    ``` hugo new site <path-to-site>    
	cd <path-to-site> ``` 
	
	2. Populate the content directory with your stuff.
		3. Files must have    a header    

            ``` +++ 
			draft=true
			title="title"
			date=date
			+++ ```

	2. Install the themes. 
    ``` git clone --recursive https://github.com/spf13/hugoThemes themes ```

	2. Run Hugo
	``` hugo server --theme=hyde --buildDrafts
	```
	You can edit your content and run Hugo again, 
	or use 
		```hugo server --theme=hyde --buildDrafts --watch```
		
		You can edit and add more content while Hugo runs in the background and rebuilds your site every time you save your edits.


Now you are ready to publish your site. Create a bare branch gh-pages at
the site you want to publish on. 
One way to do this is to 

```
git init tmp
cd tmp
touch README.md
git add README.md
git commit -m "Init"
git remote add origin ssh://git@github/duncombe/test-site.git
git push origin master:gh-pages
```

And you can throw away the tmp directory and everything it has, we do not
need it any more.

```
cd ..
rm tmp
```

Now put everything in the public directory into a subtree with a new
branch name, checkout the branch, pull to help avoid problems and push to
the site gh-pages branch.

```
git subtree split -P public -b new-gh-pages


git push test-site split-gh-pages:gh-pages
```


 1123  hugo 
 1124  ls -altr
 1126  git branch -d split-gh-pages
 1127  git branch -D split-gh-pages
 1128  git subtree split -P public -b split-gh-pages 
 1129  ls public
 1130  ls
 1131  git status
 1132  vi .gitignore
 1133  git status
 1134  git commit -a -m "Change gitignore to ignore public in this branch."
 1135  git subtree split -P public -b split-gh-pages 
 1136  ls public/
 1138  git checkout split-gh-pages 
 1139  ls -ltr

```



