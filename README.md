# ELIXIR Train The Trainers

## Welcome!

First and foremost, Welcome! 

This document (the `README` file) is a hub to give you some information about the
project. Jump straight to one of the sections below, or just scroll down to find
out more.

## How can I generate the website locally?

You need a `ruby` environment (version >= 2.4). Either you have it installed and
you know how to install [Bundler](https://bundler.io/) and
[Jekyll](https://jekyllrb.com/) and then run Jekyll, or you use
(mini-)[conda](https://conda.io/docs/index.html), a package management system
that can install all these tools for you. You can install it by following the
instructions on this page: https://conda.io/docs/user-guide/install/index.html

In the sequel, we assume you use miniconda.

1. Open a terminal
2. Clone this GitHub repository:

   ```
   $ git clone https://github.com/
   ```

3. Navigate to the `/` folder with `cd`
4. Set up the conda environment:

   ```
   $ make create-env
   ```

5. Install the project's dependencies:

   ```
   $ make install
   ```

6. Start the website:

   ```
   $ make serve
   ```

7. Open the website in your favorite browser at:
   [http://127.0.0.1:4000/](http://127.0.0.1:4000/)

## Run the link checks

To avoid dead or wrong links, run the link checkers:

```
$ make check-html
```

## Create a new blog post

To create a new blog post:

1. Create a file in the folder `_posts` with a file named following the pattern `yyyy-mm-dd-name.md`
2. Add some metadata on the top of the file

    ```
    ---
    layout: post
    title: <title of the post>
    author: <github id of the author>
    image: images/yyyy-mm-dd-name.jpg
    ---
    ```

4. Add content of the post in the file in Markdown
3. Add images in `images/posts/`

## Add an event

To create a new blog post:

1. Create a file in the folder `_events` with a file named following the pattern `yyyy-mm-name.md`
2. Add some metadata on the top of the file

    ```
    ---
    layout: event
    title: <title of the event>
    starts: <start date for the event in format yyyy-mm-dd>
    ends: <end date for the event in format yyyy-mm-dd>
    organisers:
    - <github id of the organisers>
    trainers:
    - <github id of the trainers>
    location: <location>
    ---
    ```

4. Add content of the post in the file in Markdown
3. Add images in `images/events/`

## Add someone

Add someone to the list of people:

1. Open the `_data/people.yaml` file
2. Create a new entry there (using the GitHub id, or firstname-lastname if no GitHub id) following the alphabetical order
3. Fill in information using the tags:
    - `first-name` 
    - `last-name`
    - `twitter`
    - `website`
    - `orcid`
    - `affiliation`
    - `city`
    - `country`
    - `pronouns`
    - `roles` (leader or trainer)