Minimal site created for Hugo, a static site generator

This is a bare markdown site (see https://github.com/arocks/minimal-hugo and https://arunrocks.com/minimal-hugo-site-tutorial)
smashed together with a minimal <a href="https://themes.gohugo.io/reveal-hugo/">reveal-hugo</a> presentation.

Thanks to <a href="https://www.jakewiesler.com/blog/hugo-directory-structure/">Hugo's Directory Structure Explained</a>
for its explanation of how Hugo and its content types work.  Hugo's official doc seems to focus on trees, but Jake's post helped me see the forest.

As written, this requires hugo 0.42 or later (I think).  To use with hugo 0.40 (the one that comes with ubuntu 18.04), you'll have to both rewind to a matching reveal-hugo, and avoid using the new multiple themes feature.  For instance:
- cd themes/reveal-hugo; git reset --hard 3bd0dbabe99; cd ../..
- git mv themes/bare/layouts .
- git rm -r themes/bare
- only specify theme = "reveal-hugo" in the top-level config.toml (rather than a list)
