# Maintainer: Connor Etherington <connor@concise.cc>
# ---
_pkgname=EZ
pkgname=ez
pkgver=1.0.r1
pkgrel=1
pkgdesc='Task simplificaltion aimed at increasing the speed and efficiency of common tasks'
arch=(x86_64)
url="https://gitlab.com/qYp/${_pkgname}"
license=('MIT')
depends=()
optdepends=(
  'npn: To download npm packages with 'ezdl''
  'snapd: To install snap packages with 'ezdl''
  'pip: To install python packages with 'ezdl''
  'git: To use 'ezgc' for git cloning'
  'lf: To use 'eztst's lf file-management functionality'
  'paru: To use 'ezdl' for downloading packages from the AUR'
  )
source=("https://gitlab.com/qYp/concise/-/raw/master/x86_64/${pkgname}-${pkgver}-${pkgrel}-$arch.pkg.tar.zst")
sha256sums=('SKIP')

package() {
  install -Dm775 usr/bin/* -g wheel -o ${USER} -t "${pkgdir}/usr/bin/"
  install -Dm644 usr/share/licenses/${pkgname}/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 usr/share/doc/${pkgname}/* -t "${pkgdir}/usr/share/doc/${pkgname}/"
}
