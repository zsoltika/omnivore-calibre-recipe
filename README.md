## Omnivore-calibre-py

The purpose is to have valid EPUB ebooks of my Omnivore articles.

You need to have Calibre and `omnivoreql` installed (as a system python
package since `calibre` could only import it that way - or there might be
other ways, that I did not investigated yet.

You have to set (e.g. in your `.bashrc` an environment variable that points
to a file that has (only) your Omnivore API key, e.g.:

    export OMNICALAPIKEY="$HOME/API.key"

With this set up, you can run the CLI provided by Calibre to get a nicely 
formatted (and valid) EPUB file:

    ebook-convert o.recipe Omnivore-$(date +%F).epub \
        --output-profile kindle \
        --smarten-punctuation \
        --change-justification justify \
        --title "Omnivore archive" \
        --toc-title "Table of Contents" \
        --remove-paragraph-spacing-indent-size 1.3


