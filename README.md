# Rewilding Mathematics website - beta

This repository contains the source code for the **beta** version of the [Rewilding Mathematics website](https://jmarshrossney.github.io/rewilding-mathematics-beta).

## Contributing

These instructions are for individuals who participated in the Rewilding Mathematics seminar/workshop series.

In each case, create or edit the relevant Markdown (`.qmd`) file(s) using any text editor, then do one of the following:

- Post them in the *website* channel in the *Rewilding Mathematics* Discord server
- Submit a pull request to merge the additions to the `main` branch
- If neither of these options work for you, you can email me directly


### File structure

The basic structure of a file is a YAML header, which is enclosed by a pair of lines containing only `---` and contains metadata about the file, followed by a Markdown body.

```markdown
---
title: Hello World
date: 2024-06-21
author: Joe
description: This is a YAML header containing metadata.
---

## Hello World

Hello world, this is Markdown.

...
```

#### YAML header

The YAML header contains the metadata about the file in the general format `field: value`.
Any lines in which the `value` part looks like `<<TEXT GOES HERE>>` *must* be modified by either replacing the `<<TEXT GOES HERE>>` part with your text, or deleting the entire line.

In the YAML header:
- Indentation is important; do not change the indentation of any line
- Any lines beginning with `#` are treated as comments


#### Markdown body

Writing in [Markdown](https://www.markdownguide.org/) when you're used to LaTeX or Word is embarassingly easy.

This blog is based on [Quarto](https://quarto.org/) which uses an [extended Markdown syntax](https://pandoc.org/MANUAL.html#pandocs-markdown) with some nice additional functionality.
The best place to look for guidance is the [Quarto guide](https://quarto.org/docs/guide/).


### Adding or updating your profile on the 'people' page

If you do not already have a profile, copy the file `templates/profile.qmd` into the `people/` directory and rename it in the format `Firstname_Surname.qmd`.

Modify this file as you wish, or by following the guidance inside the file.

To add a profile photo, you need to modify *both* of the relevant lines, so that they read `image: https://link/to/your/profile/photo.jpg` (if you are using a photo that is already online) or `image: /assets/images/Firstname_Lastname.jpg` (if you are uploading a new photo).

See [Adding Photos](#adding-photos) for further guidance.


### Add a blog post

Copy `templates/blog_post.qmd` to the `posts/` directory, editing or deleting the fields in the YAML header as required.
Provided you add a valid date, your post will automatically appear in the `Blog` listing when it is merged with the `main` repository branch.

### Add a news item

This is exactly the same deal as with the blog post, but the `templates/news_item.qmd` template should be copied into the `news/` directory as opposed to the `posts/` directory.

### Adding images

There are two options for adding images

#### Option 1 (preferred, for now): A photo that is already online

Right-click on the photo and select *copy image address*.
Display the image in your post using the syntax `![alt text](https://link/to/your/photo.jpg)`.

Note that the link should end in `.jpg` or `.png` - vector images won't work.

#### Option 2: Use a local photo

For now, send the photo to me.
Use the syntax `![alt text](/assets/images/<image_name>.jpg)` in your file where you want the image displayed.

In future This should not be so awkward in future but I want to avoid committing lots of photos to version control before we settle in.


## Building the website locally

If you intend to write a blog post or news item, it is very helpful to be able to build the website locally to see how everything looks.

The only thing you need to build this website locally is [Quarto](https://quarto.org/).
In the root of the cloned repository, run `quarto preview` to render and preview the site.
With a few exceptions, any changes you make to the source files (`.qmd`) will be immediately reflected in the website preview.
See [further instructions](https://quarto.org/docs/websites/#website-preview) on previewing Quarto websites.


## Queries

If you are on the *Rewilding Mathematics* Discord server, feel free to ask any questions on the *website* channel.

Alternatively, raise an issue on GitHub, or email me directly.
