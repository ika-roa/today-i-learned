# Reloading packages in Jupyter

If you already imported a module and you try to import it again, Python will ignore this request. In order to reload packages during development, write into the first code cell:

```
%load_ext autoreload

%autoreload 2
```

And each time you execute some code, IPython will reimport all the modules to make sure that you are using the latest possible versions.

There are 3 configuration options that you can set:

-   `%autoreload 0` - disables the auto-reloading. This is the default setting.
-   `%autoreload 1` - it will only auto-reload modules that were imported using the `%aimport` function (e.g `%aimport my_module`). It's a good option if you want to specifically auto-reload only a selected module.
-   `%autoreload 2` - auto-reload all the modules. Great way to make writing and testing your modules much easier.