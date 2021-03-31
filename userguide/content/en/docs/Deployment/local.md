---
title: "Serving your site locally"
linkTitle: "Serving your site locally"
weight: 1
description: >
  Deploy your site locally
---

Depending on your deployment choice you may want to serve your site locally
during development to preview content changes. To serve your site locally:

1.  Ensure you have an up to date local copy of your site files cloned from
    your repo. Don't forget to use `--recurse-submodules` or you won't pull
    down some of the code you need to generate a working site.

    ```
    git clone --recurse-submodules --depth 1 https://github.com/my/example.git
    ```
   
    {{% alert title="Note" color="primary" %}}If you've just added the theme 
    as a submodule in a local version of your site and haven't committed it to
    a repo yet,  you must get local copies of the theme's own submodules before
    serving your site.
    
    git submodule update --init --recursive{{% /alert %}}

1.  Ensure you have the tools described in [Prerequisites and
    installation](/docs/getting-started/#prerequisites-and-installation)
    installed on your local machine, including `postcss-cli` (you'll need it to
    generate the site resources the first time you run the server).

1.  Run the `hugo server` command in your site root. By default your site will
    be available at http://localhost:1313/.

Now that you're serving your site locally, Hugo will watch for changes to the
content and automatically refresh your site. If you have more than one local
git branch, when you switch between git branches the local website reflects the
files in the current branch.


