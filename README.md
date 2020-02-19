# Information
This is a test repository to get up to speed with MkDocs and ReadTheDocs.

Initial inspiration on how to link these came from https://varrette.gforge.uni.lu/blog/2018/01/18/tutorial-mkdocs-and-readthedocs/.
However, the step 
> Go to 'Settings / Integrations & services', select “Add service” and select ‘ReadTheDocs’.

is no longer an option as this functionality seems to have been deprecated in GitHub in the favor of using webhooks.

Instead, I followed https://readthedocs.org/accounts/social/connections/ and selected "Connect on GitHub" which redirected to the GitHub authorisation-of-a-third-party page.
There, I needed to allow readthedocs to connect.
Following this, I went to https://readthedocs.org/dashboard/ and clicked on the "Import a project" button.
From the list of my repositories, I selected the one of interest (https://github.com/claczny/rtd-mkdocs-test), clicked on the "+" button and did some basic set-up.
This automatically added the respective webhook to the GitHub repository, which can be seen on the repo-page -> "Settings" -> "Webhooks".

Alternatively, following the instructions at https://docs.readthedocs.io/en/stable/webhooks.html#github should probably also work, but I found the above simpler.

The first build succeeded, but seems to have been a dummy built, using `Sphinx` instead of `MkDocs`.
I then went back to the RTD dashboard, selected the newly created project (`embo2020-rtd-mkdocs-test`), clicked on "Admin" -> "Advanced settings" ->"Documentation type" and changed this to "MkDocs (Markdown".
