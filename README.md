# Your Portfolio • [portfolio-base](//github.com/fenollp/portfolio-base)

Be sure you understand what you are doing. No actually, it really doesn't matter.

Note: the base portfolio is actually a website published at https://fenollp.github.io/portfolio-base/

## Syntax

You can put HTML anywhere you want!

But more fun is to write [MarkDown code](//help.github.com/articles/github-flavored-markdown)!
Note that said code can only be put thusly:

```html
    <div id="content" data-markdown>
      [![my subtitle](myfoder/my_picture_SMALL.jpg "My Text Displayed on Hover")](myfolder/my_pic_LARGE.jpg)


      **Some text in bold**
    </div>
```

That is: your markdown has to be written in between `<div id="content" data-markdown>` and `</div>`, otherwise it will not be displayed properly.

## Menu

Edit `meta/menu.js` to provide links / sections that will always figure on the left part of every page.
The Menu is to be written in MarkDown too.


## Adding Pages

The easiest to add pages is to:
1. create a folder named after the new section you are creating (e.g.: `art2016`)
1. copy-paste one page that you like in this folder
1. name the new page `index.htm`
    * Note: the page is now accessible under `art2016/index.htm`
1. put pictures in the folder
1. edit the page's content to add text, links, videos, the images, …
1. open a terminal window and drag-and-drop `sync.sh` there then hit ENTER

Your new page should be pushed and the website updated in at most 10 minutes.

The page will be accessible at `My_Website/art2016/` where `My_Website` can be
* `http://MY_GITHUB_USERNAME.github.io/MY_GITHUB_REPO_NAME`
* or also: starting with `https` instead of `http`

For instance, if you just *cloned* the `portfolio-base` repo and your GitHub username is `mee`:

    https://mee.github.io/portfolio-base/art2016

…is the link to your new page!

Note: `a_folder/` is the same as `a_folder/index.htm`: the *thing* knows you are looking inside `a_folder` and will automatically look for the `index.htm` page for you.
You could name the page differently of course (e.g.: `my_page.htm`) as long as it contains only alphanumerical characters (**but folders and filenames must not contain spaces!**.


## Testing

Before `sync.sh`-ing your changes and to save iteration time, you may want to “test” your website locally.

To do so, open the `Terminal` and:
1. `cd` into your portfolio project
1. start a simple daemon: `python -m SimpleHTTPServer 1337`
1. Open your browser at http://localhost:8080


## Using a Domain Name

Buy a domain name (`something.me`, `bla.fr`, `coucou.in`, …) at a place like [//domain.bzctoons.net](//domain.bzctoons.net) or OVH.

Once you bought your own domain name, like: `mywebsite.com`, you can set up your domain name provider's DNS to redirect to your portfolio project.

To do so,
1. Edit `CNAME` and replace `mywebsite.com` with your own domain (don't forget to `sync.sh`)
1. On the DNS panel, add a **CNAME Record** with Name: `mywebsite.com` & Value: `MY_GITHUB_USERNAME.github.io`
1. You may also need to set up 2 **A Records** with Name: `mywebsite.com` & Values: `192.30.252.153` & `192.30.252.154`

Troubleshooting: //help.github.com/articles/setting-up-a-custom-domain-with-github-pages


### This all relies on

https://pages.github.com/

❤
