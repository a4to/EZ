# Maintainer: Connor Etherington <connor@concise.cc>
# ---
_pkgname=EZ
pkgname=ez
pkgver=1.0.3
pkgrel=1
pkgdesc='Task simplificaltion scripts for increasing the speed and efficiency of common tasks'
arch=(x86_64)
url="https://gitlab.com/a4to/${_pkgname}"
license=('MIT')
depends=()
optdepends=(
  'npn: To download npm packages with 'ezdl''
  'snapd: To install snap packages with 'ezdl''
  'python-pip: To install python packages with 'ezdl''
  'git: To use 'ezgc' for git cloning'
  'lf: To use 'eztst's lf file-management functionality'
  'paru: To use 'ezdl' for downloading packages from the AUR'
  )
provides=(ezdl ezgc eztst)
source=("git+$url.git")
sha256sums=('SKIP')

package() {
  cd "${_pkgname}"
  install -Dm775 usr/bin/* -g wheel -o ${USER} -t "${pkgdir}/usr/bin/"
  install -Dm644 usr/share/licenses/${pkgname}/LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 usr/share/doc/${pkgname}/* -t "${pkgdir}/usr/share/doc/${pkgname}/"
}
