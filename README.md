# What is yrPublish?

The project in this repo is currently called yrPublish. That name many
change in the future.

yrPublish is a publishing system that enhances the features of the Quarto
publishing system. yrPublish, under the covers, uses Quarto as the
primary publishing system. However, Quarto is limited in some respects
that this system tries to address.

## What is Quarto?

Quarto is a publishing system that can render entire projects into structured outputs
such as:

- Websites
- Books
- Manuscripts

It allows for output formats of HTML, PDF, Word and other formats.

## What does this repo add?

This repo attempts to address the following
limitations of Quarto (as of today, March 20, 2026).
There may be additional features added in the future.

- Quarto books cannot have custom chapter numbers. Chapter numbers always
  start from 1 and are sequential. This repo adds the ability to have custom
  chapter numbers.

- Quarto books have "chapters". Large books with many chapters can segment
  the chapters of a book among different "part"s of the book. However, there is no
  way to have nested parts for books that become much larger.

  One of the goals of this project is to allow for a much deeper nesting
  of a hierarchical organization scheme for very large books.

## More about yrPublish

In general yrPublish adds several assets and imposes some constraints on how to
create publishable content. There are some Bash scripts, custom css and javascript etc
that are used with this system.

The general workflow to render a book built with this system is:

1. Create the repo using the `yrPublish.sh create-project my-project` to create a new repo.
   This is similar to the similar quarto command.

2. The yrPublish.sh command creates the folder structure and adds any files
   or assets that are needed for a new project.

3. Content creators add content in the same general way that they would for
   quarto files. This includes editing .qmd files, creating a _quarto.yml file,
   etc. However, content editors that are using the yrPublish system should
   make sure to adhere to the yrPublish guidelines. For example, if a content
   creator wants custom chapter numbers for their book they should follow
   the directions in the docs for yrPublish to do so. Currently this includes

   - editing the _quarto.yml file with special directives to
     record the custom chapter numbers

   - running some yrPublish specific scripts prior to rendering the project
     with the quarto cli tools. The entire process is documented in the
     yrPublish docs folder.

## Documentation for yrPublish

The docs folder in this repo contains a quarto book with the documentation
for this system. It also includes any specs for updates to the yrPublish system
itself.

## Goal is to be a quarto compliant as possible

Note that the Quarto system is under ongoing development and may add
features in the future that yrPublish had already added.

If/when that happens the goal of this system is prefer yrPublish projects
to use the native Quarto features as much as possible. The goal of yrPublish is
NOT to reinvent the wheel (at least not yet) but to add features to Quarto
where they are missing.
