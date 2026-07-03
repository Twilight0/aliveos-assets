# Maintainer: Twilight <twilight@aliveos.org>
# NOTE: This PKGBUILD is for the standalone aliveos-assets project.
# When building inside aliveos-repo, use packages/aliveos-assets/PKGBUILD
# which sources from this repo's release archive.

pkgname=aliveos-assets
pkgver=1.0.0
pkgrel=1
pkgdesc="Distro identity assets for AliveOS: neon dark square icon theme, wallpapers, and system logo"
arch=('any')
url="https://github.com/Twilight0/aliveos-assets"
license=('GPL3')
depends=('hicolor-icon-theme')
optdepends=('papirus-icon-theme: fallback icon theme for icons not in aliveos set')
source=()
sha256sums=()

package() {
  # --- Icon theme ---
  # Installs the complete aliveos icon theme tree (icons + index.theme + symlinks)
  install -d "${pkgdir}/usr/share/icons/aliveos"
  cp -a "${startdir}/icons/aliveos/." "${pkgdir}/usr/share/icons/aliveos/"

  # --- System logo (pixmaps) ---
  # Used by org.cinnamon system-icon and other distro-identity references.
  # Placed in /usr/share/pixmaps which is the canonical location for
  # standalone logos per the XDG icon theme spec.
  install -Dm644 "${startdir}/pixmaps/aliveos-logo.png" "${pkgdir}/usr/share/pixmaps/aliveos-logo.png"

  # --- Wallpapers ---
  # Multiple aspect ratios for different screen sizes.
  install -d "${pkgdir}/usr/share/backgrounds/aliveos"
  cp -a "${startdir}/backgrounds/aliveos/." "${pkgdir}/usr/share/backgrounds/aliveos/"
}