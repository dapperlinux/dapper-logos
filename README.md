# dapper-logos

##About
The Dapper Logos package contains the icons for the Dapper Linux distrubution, and are used in the boot process with plymouth, branding in gnome-shell and gnome-settings, and in the installer, ananconda.

This package is based off of the generic-logos package and fully complies with necessary conditions to make a Fedora Remix.

##Building
To build this package, first install an RPM development chain:

```bash
$ sudo dnf install fedora-packager fedora-review

```

Next, setup rpmbuild directories with

```bash
$ rpmdev-setuptree
```
And place the file dapper-logos.spec in the SPECS directory, and rename the dapper-logs directory to dapper-logos-1 and compress it:
```bash
$ mv dapper-logos.spec ~/rpmbuild/SPECS/
$ mv dapper-logos dapper-logos-25.0
$ tar -czvf dapper-logos-25.0.tar.gz dapper-logos-25.0
$ mv dapper-logos-25.0.tar.gz ~/rpmbuild/SOURCES/
```

and finally, you can build RPMs and SRPMs with:
```bash
$ cd ~/rpmbuild/SPECS
$ rpmbuild -ba dapper-logos.spec
```


