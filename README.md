# hugo-eclipsefdn-website-boilerplate

This boilerplate was created to help Eclipse Projects migrate their website to Hugo!

We've ensured that this project is compatible with `Hugo 0.110.0`. For information on the specific versions of Hugo we support, you can refer to the [readme.md](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-solstice-theme#getting-started) of our [Hugo Solstice Theme](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-solstice-theme) project.

## Getting started

Clone the project with submodules and start a web server:

```bash
git clone --recurse-submodules https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-eclipsefdn-website-boilerplate.git
cd hugo-eclipsefdn-website-boilerplate
hugo server
```

### Update hugo-solstice-theme

The [hugo-solstice-theme](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-solstice-theme) was added to this project as a git submodule. We recomend that you update to the latest version before getting started:

```bash
git submodule update --remote
```

Please make sure to keep this sub-module up-to-date if you decide to utilize it. The Eclipse Foundation Webdev team regularly publishes new versions. For more information, please see git documentation on [submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

## How to build my project's website with Jenkins?

The preferred static website generator for Eclipse project websites is [Hugo](https://gohugo.io/) and we recommend to our projects that they get started by creating a copy of our [hugo-eclipsefdn-website-boilerplate](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-eclipsefdn-website-boilerplate) project. While you're not obligated to use them, please note that Hugo and hugo-eclipsefdn-website-boilerplate are the supported solutions by the Eclipse Foundation. Using a different technology may result in reduced support.

In this setup, you'll need two Git repositories. The first one contains your Hugo website's source code, which you can obtain by cloning this repo. The second repository stores your Hugo build results, essentially the static HTML that our web server will end up hosting. Once you've completed the initial setup, managing two repos isn't a concern because the second one will be automatically updated via the `Jenkinsfile`.

If you don't already have two git repositories for your website, you can request them to be created by [opening a ticket](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/new?issuable_template=project-website).

Before deploying your website, you must update the `Jenkinsfile` at the root of this repository with the correct values for the `PROJECT_NAME` and `PROJECT_BOT_NAME` environment variables. Additionally, it's important to update the `README.md`, `config.toml`, and all files in the `content` folder. Remember, this is just a boilerplate to kickstart your project; you'll still need to create pages and content.

If you don't have a Jenkins instance already, [ask for one](https://wiki.eclipse.org/CBI#Requesting_a_JIPP_instance).
Please note that the `Jenkinsfile` file example makes several assumptions. For instance, it assumes that your project will use main as the default branch and that you are using Gerrit to publish your build results. Projects must customize the file to suit their specific requirements and configurations.

If you're new to Hugo, I highly recommend checking out its [documentation](https://gohugo.io/documentation/) to learn how to create pages and customize your site. Although you're starting with [hugo-solstice-theme](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-solstice-theme), remember that Hugo is highly extensible, allowing you to override as much or as little as you need. For example, you may choose to keep our default footer but override our header. You can make as many changes as you want as long as your website continues to adhere to the [Eclipse Foundation Hosted Services Privacy and Acceptable Usage Policy](https://www.eclipse.org/org/documents/eclipse-foundation-hosted-services-privacy-and-acceptable-usage-policy.pdf).

Finally, to publish your website on eclipse.dev, you'll need support from us to update your project's website metadata in the [projects.eclipse.org](https://projects.eclipse.org/) (PMI). This informs us on where to find the necessary static HTML to serve. You can request an update to your website deployment metadata by [opening a ticket](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/new?issuable_template=project-website).

 If you need assistance with the process, [open a ticket](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/new?issuable_template=project-website).

## Contributing

1. [Fork](https://docs.gitlab.com/ee/user/project/repository/forking_workflow.html) the [hugo-eclipsefdn-website-boilerplate](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-eclipsefdn-website-boilerplate) repository
2. Clone repository: `git clone --recurse-submodules https://gitlab.eclipse.org/[your_gitlab_username]/hugo-eclipsefdn-website-boilerplate.git`
3. Create your feature branch: `git checkout -b my-new-feature`
4. Commit your changes: `git commit -m 'Add some feature' -s`
5. Push feature branch: `git push origin my-new-feature`
6. Submit a pull request

### Declared Project Licenses

This program and the accompanying materials are made available under the terms
of the Eclipse Public License v. 2.0 which is available at
http://www.eclipse.org/legal/epl-2.0.

SPDX-License-Identifier: EPL-2.0

## Related projects

### [solstice-assets](https://gitlab.eclipse.org/eclipsefdn/it/webdev/solstice-assets)

Images, less and JavaScript files for the Eclipse Foundation look and feel.

### [hugo-solstice-theme](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-solstice-theme)

Hugo theme of the Eclipse Foundation look and feel.

## Bugs and feature requests

Have a bug or a feature request? Please search for existing and closed issues. If your problem or idea is not addressed yet, [please open a new issue](https://gitlab.eclipse.org/eclipsefdn/helpdesk/-/issues/new).

## Author

**Christopher Guindon (Eclipse Foundation)**

- <https://twitter.com/chrisguindon>
- <https://github.com/chrisguindon>

## Trademarks

* Eclipse® is a Trademark of the Eclipse Foundation, Inc.
* Eclipse Foundation is a Trademark of the Eclipse Foundation, Inc.

## Copyright and license

Copyright 2021 the [Eclipse Foundation, Inc.](https://www.eclipse.org) and the [hugo-eclipsefdn-website-boilerplate authors](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-eclipsefdn-website-boilerplate/-/graphs/main). Code released under the [Eclipse Public License Version 2.0 (EPL-2.0)](https://gitlab.eclipse.org/eclipsefdn/it/webdev/hugo-eclipsefdn-website-boilerplate/-/blob/main/LICENSE).
