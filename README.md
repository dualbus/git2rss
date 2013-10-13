git2rss
=======

Fork of git2rss, an RSS feed generator for the activity of a git
repository. Original source http://bent.latency.net/git2rss by
Bennett Todd.


Usage
-----


    --description=DESCRIPTION
            Use DESCRIPTION as the description of the RSS feed. If
            this option is omitted, it will attempt to read the
            repo/.git/description file or bare/description file, and
            use the body as the description. The first line isn't
            used for the description, since it's taken to be the
            title of the repository.

    --email=EMAIL
            Specify the email of the webmaster responsible for the
            RSS feed. If omitted, it will default to postmaster@HOST,
            where HOST is the hostname part of URL.

    --max=MAX
            This option is used to limit the amount of items in the
            RSS feed. Only MAX number of elements will be output.

    --title=TITLE
            Use TITLE as the title of the RSS feed, or default to the
            first line of the description file in the git repository
            if this option is not provided.

    --url=URL
            This option is mandatory. It's used as the base URL for
            all the items in the RSS feed.


Environment
-----------

    GIT_DIR
            git2rss uses the GIT_DIR environment variable to
            determine the location of the git repository, and it
            chdir's to that location before running any command. This
            will allow you to run the script from other locations.
            git2rss will unset the GIT_DIR variable before running
            any git command.

Examples
--------

    GIT_DIR=~/local/src/git2rss/.git git2rss --url https://github.com/dualbus/git2rss
