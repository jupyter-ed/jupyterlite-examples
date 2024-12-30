# jupyterlite-examples

The examples are to study the size of the final build for variant environment.yml:

- minimal size is around 5MB for the case with just the jupyterlite core, which gives the basic functionality like text/markdown editor.
- for environment_data.yml, the xeus case gives around 60MB.
- the number of xhr/fetch requests ends up around a few hundred per session. max-age is set to 600s for all files by default. A great article on cache headers and service-worker basics is [here](https://jakearchibald.com/2016/caching-best-practices/).
- the numbers correspond to jupyterlite CLI opions --no-source-maps and --no-unused-shared-packages
- no contents (notebooks) were used in the build.
