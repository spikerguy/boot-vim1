# Maintainer: Dan Johansen <strit@manjaro.org>
# Contributor: Spikerguy <shareahack@hotmail.com>
pkgname=boot-vim1
pkgver=2019.08
pkgrel=1
pkgdesc="Required boot files for Khadas Vim 1"
arch=('aarch64')
url='http://manjaro.org'
license=('GPL')
depends=('uboot-tools')
source=('aml_autoscript'
        'aml_autoscript.zip'
        'emmc_autoscript'
        'emmc_autoscript.cmd'
        's905_autoscript'
        's905_autoscript.cmd'
        'uEnv.ini'
        '91-uInitrd.hook')
md5sums=('6776dadefe1b7b9031a83dec77f91efa'
         'da3eb7f21ec07932e82416a9c86267dd'
         '4982ebcfe01eaeb22e294af7b03dd215'
         '4f186a8f63cbd169474c3f4f89c78a26'
         '252635687b7d70dfb149a5697dd51c7c'
         '5de7aacbc7b1a026cb7e51cebab8010f'
         '0b2b09ab001156e9a575f3e19f32ebe3'
         '1a6c88e2ede5ee7fc0c1ad97275c6f5d')

package() {

  mkdir -p "${pkgdir}"/boot
  cp aml_autoscript aml_autoscript.zip emmc_autoscript emmc_autoscript.cmd uEnv.ini s905_autoscript s905_autoscript.cmd "${pkgdir}"/boot
  
    sed "${_subst}" ../91-uInitrd.hook |
    install -Dm644 /dev/stdin "${pkgdir}/usr/share/libalpm/hooks/91-uInitrd.hook"
}
