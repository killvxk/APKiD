# APKiD

This tool gives you information about how an APK was made. It identifies many compilers, packers, and obfuscators. _It's [PEiD](https://www.aldeid.com/wiki/PEiD) for Android._

# Installing

```bash
pip install --process-dependency-links apkid
```

The `--process-dependency-links` option is temporarily necessary to install our custom fork of [`yara-python`](https://github.com/rednaga/yara-python) rather than the official version. Our fork contains a [module](https://github.com/rednaga/yara/blob/master/libyara/modules/dex.c) we developed for processing dex files. This should be removed in a future release.

# Licensing

This tool is available under a dual license: a a commercial one suitable for closed source projects and a GPL license that can be used in open source software.

Depending on your needs, you must choose one of them and follow its policies. A detail of the policies and agreements for each license type are available in the LICENSE.COMMERCIAL and LICENSE.GPL files.

# Hacking

To install the package from source in editable mode (useful for devlopment):

```bash
pip install --process-dependency-links -e .
```

If the above doesn't work, due to permission errors dependant on your local machine and where Python has been installed, try specifying the `--user` flag. This is likely needed if you are working on OSX;

```bash
pip install --process-dependency-links -e . --user
```