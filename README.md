# A simple and static site to test deadlinkchecker script

This repository provides a sample website to [https://github.com/JeremieLitzler/linkprobe](https://github.com/JeremieLitzler/deadlinkprobe) project.

## Goal 

generate a very simple static website structure to test a script I'll create that does the following:

```plaintext
With an input being a URL, scan the website for all internal and external links.

For external links, do not continue scanning, For internal links, continue scanning until all links have been discoverrd.

Then, check all links to gather HTTP status code.

The output is a CSV for the run with the link itself, the referrer link, the HTTP status code.

Try to run the logic with parallel requests.
```

The goal is to create a set of a few HTML files to test:
* an index file linking to several pages
* a sub page pointing to another sub page that is not in the index
* a sub page must contains a link to a not existing sub page (to test 404)
* a page must contains an external link to a valid page (ex: http://iamjeremie.me/) and a not existing page (http 404. Ex: http://iamjeremie.me/doesnt-exist)

I want to host this on netlify to use in the script elaboration. 

the script to check a website is out of scope.
