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


Now you are ready to publish your site. Create a bare branch ```gh-pages``` at
the site (```github.com/<account-owner>/<repository>```) that you want to publish on (to appear at ```<account-owner>.github.io/<repository>```).  
One way to do this is to create a bare repository and push it to gh-pages branch at github: 

```
git init tmp
cd tmp
touch README.md
git add README.md
git commit -m "INITIAL commit on gh-pages branch."
git remote add origin ssh://git@github.com/<account-owner>/<repository>.git
git push origin master:gh-pages
```

And you can throw away the tmp directory and everything it has, we do not
need it any more.

```
cd ..
rm -rf tmp
```

Now put everything in the public directory into a subtree with a new branch name, checkout the branch, pull to help avoid problems, and push to the site gh-pages branch. In the context of the sos-guidelines being published with Hugo (at the remote  `test-site`, say),  

```
git subtree split -P public -b new-gh-pages
```
`new-gh-pages` must not exist.

```
git push test-site new-gh-pages:gh-pages
```

Some things you might have to do to get the files onto the gh-pages branch at the repository on github (i.e., to get the push to work):
While on the branch ``new-gh-pages``
``` git pull test-site gh-pages ```
or you might as a last resort force the push possibly messing up a bunch of stuff, but it is only a `gh-pages` branch and hopefully no one (else) will be pulling from or pushing to.

`new-gh-pages` is a temporary thing. Usually throw it away when you are done with it. 
```git branch -d new-gh-pages```
or (forcefully)
```git branch -D new-gh-pages```



```



