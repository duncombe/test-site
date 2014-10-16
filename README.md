sos-guidelines
==============

## Creating and updating sos-guidelines web-pages

1. Use Hugo 
  2. Get and install Hugo from
[gohugo.io](http://gohugo.io/overview/quickstart/), Step 1.   
  2. Following the quickstart Guide, have hugo create a site    
```hugo new site <path-to-site>    
cd <path-to-site>```
	3. Populate the content directory with your stuff.
		4. files must have    a header    
```
	+++ 
	draft=true
	title="title"
	date=date
	+++
```

	3. Install the themes

```
	git clone --recursive https://github.com/spf13/hugoThemes themes
```

	3. Run Hugo

```
	hugo server --theme=hyde --buildDrafts
	2 pages created
	0 tags created
	0 categories created in 5 ms
	Serving pages from exampleHugoSite/public
	Web Server is available at http://localhost:1313
	Press ctrl+c to stop
```

You can edit your content and run Hugo again, 

	3. or use 

```hugo server --theme=hyde --buildDrafts --watch```

Now you can edit and add more content while Hugo runs and builds
your site everytime you save your edits.

