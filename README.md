### Install dependencies

dnf build-dep gnome-shell
dnf install rpm-build rpmdevtools

### Set up environment

rpmdev-setuptree

### Download source tarball

spectool --define "_sourcedir $PWD" -g -R gnome-shell.spec

### Build

rpmbuild --define "_sourcedir $PWD" -ba gnome-shell.spec 
