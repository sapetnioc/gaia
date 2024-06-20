![Build Static Pages](https://github.com/neurospin/gaia/workflows/Build%20Static%20Pages/badge.svg)

# Configuration

You have to customize the following parameters in `_config.yml`:

- title: the name of your team.
- subtitle: the runing title.
- email: the contact email.
- short_desc: the title of the banner in the index page.
- long_desc: the content of the banner in the index page.
- expiration_opportunities: the job offers will expire automatically after this number of days.
- expiration_news: the news will expire automatically after this number of days.

You can change the banner image in the index page `images/banner.png` and the logo `images/logo.png`.

Then you will need to fill the collections in `_collections` (only text files).
Please look at the example and use the same keys.

Note: For the research collection, you will have to add a new `research_<CATEGORY>.md` for new categories.

# Install local

Jekyll:

- sudo apt install ruby-dev
- echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
- echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
- echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
- source ~/.bashrc
- gem install jekyll bundler
- cd $MYPROJECT
- bundle init
- bundle add jekyll webrick
- bundle install
- bundle exec jekyll serve --livereload --port 8080


For Bibtex conversion:

- pip install pybtex
- pybtex-convert biblio.bib biblio.yaml

# Jekyll

For those unfamiliar with how Jekyll works, check out [https://jekyllrb.com/](https://jekyllrb.com/) for all the details.
