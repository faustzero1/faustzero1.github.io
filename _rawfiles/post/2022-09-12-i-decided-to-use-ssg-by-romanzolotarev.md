<nav>
<a href="../index.html">Home</a>
|
<a href="../post.html">Post</a>
|
<a href="../project.html">Project</a>
|
<a href="../about.html">About</a>
|
<a href="../contact.html">Contact</a>
</nav>
</header>
<hr><hr>
<main>
<!-- Your Content Start After This Line -->


# I decided to use ssg by romanzolotarev #NOTFINISHEDYET

Date published: 2022-09-12

---

## What is *ssg*

**ssg** is a simple Static Site Generator written in POSIX shell. <br>
Created by Roman Zolotarev.

How it works is just like a sandwich, there is:

1. "_header.html" file 			=> Top part of the sandwich
2. "2022-09-12-your_content.md" file 	=> Middle part of the sandwich
3. "_footer.html" file 			=> Bottom part of the sandwich

---

## Guide how to install and use *ssg*

### Download & install *ssg* & *Markdown.pl*

We will install **ssg** and **Markdown.pl** at ```/home/$USER/.local/bin/<here>``` <br> 
Please make sure that directory is on your $PATH.

Install it with this command:

```
$ curl -s https://rgz.ee/bin/ssg > /home/$USER/.local/bin/ssg <br>
$ curl -s https://rgz.ee/bin/Markdown.pl > /home/$USER/.local/bin/Markdown.pl
```

Allow file execution permission for those files:

```
$ chmod +x /home/$USER/.local/bin/ssg <br>
$ chmod +x /home/$USER/.local/bin/Markdown.pl
```

### Usage

The basic command usage are ```ssg /src /dst 'Website | Title' 'https://yourwebsiteurl.org' <br>
This is how I use *ssg*, for example we are going to make:

* Source directory at pages/_rawdata/
* Destination directory at pages/
* The content of the website is '# Hello world'
* The markdown name is 2022-09-first-post.md
* The website title is 'Harambe | Cool'

So, the commands is:

```
$ mkdir pages 
$ cd pages
[pages] $ 
[pages] $ mkdir _rawdata/
[pages] $ echo '<html><title></title><body>' > _rawdata/_header.md
[pages] $ echo '</body></html>' > _rawdata/_footer.md
[pages] $ echo '# hello world!' > _rawdata/2022-09-12-first-post.md
[pages] $ ssg _rawdata/ . 'Harambe | Cool' 'https://harambeiscool.org'
./2022-09-12-first-post.md
[ssg] 1 files, 1 url
```

### Test your website
 
Open the html file has been created on your browser

```
[pages] $ firefox 2022-09-12-first-post.md
```
---

Reference: <br>
[Romanzolotarev Blog](https://romanzolotarev.com/ssg.html) <br>
[Wolfgangs Channel (Youtube)](https://www.youtube.com/watch?v=N_ttw2Dihn8)
