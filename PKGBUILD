# Main maintainers of the GTK-3 counterpart:
# Maintainer: Thomas Lange <thomas-lange2@gmx.de>
# Contributor: Evangelos Foutras <evangelos@foutrelis.com>
# Contributor: Gaetan Bisson <bisson@archlinux.org>
# Contributor: Alexander Fehr <pizzapunk gmail com>
# Contributor: Giovanni Scafora <giovanni@archlinux.org>

# Changed a single line of code
# Contributor: JohnTWD <@fatmc1209 (dc)>

_pkgname=audacious
pkgname=$_pkgname-gtk2
pkgver=4.5.1
pkgrel=1
pkgdesc="Lightweight, advanced audio player focused on audio quality (GTK-2 version)"
arch=('i686' 'x86_64')
url="https://audacious-media-player.org/"
license=('BSD')
depends=('gtk2' 'glib2')
makedepends=('meson' 'glib2-devel') # for gdbus-codegen
optdepends=('unzip: zipped skins support')
provides=("$_pkgname")
conflicts=("$_pkgname")
install="$_pkgname.install"
source=("https://distfiles.audacious-media-player.org/$_pkgname-$pkgver.tar.bz2")
sha256sums=('7194743a0a41b1d8f582c071488b77f7b917be47ca5e142dd76af5d81d36f9cd')

build() {
  arch-meson $_pkgname-$pkgver build \
    -Dqt=false \
    -Dgtk2=true \
    -Dbuildstamp='Arch Linux (GTK-2)'
  meson compile -C build
}

package() {
  meson install -C build --destdir "$pkgdir"
  install -Dm644 $_pkgname-$pkgver/contrib/audacious.appdata.xml -t "$pkgdir/usr/share/metainfo"
  install -Dm644 $_pkgname-$pkgver/COPYING -t "$pkgdir/usr/share/licenses/$_pkgname"
}
