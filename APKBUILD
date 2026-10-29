# Maintainer: YourLocalTechGuy <yourlocaldevguy@gmail.com>
pkgname=firmware-samsung-a22x
pkgver=1.0
pkgrel=0
pkgdesc="Samsung Galaxy A22 5G firmware blobs"
arch="aarch64"
url="https://postmarketos.org"
license="proprietary"
options="!check !strip !archcheck !spdx !tracedeps"
source="
    firmware.tar.gz
"

package() {
    # Create your target postmarketos search directory
    install -dm755 "$pkgdir/lib/firmware/postmarketos"
#    install -Dm644 "$srcdir/99-blobs.files" "$pkgdir/usr/share/mkinitfs/files-extra/99-blobs.files"
    # Extract or copy your firmware files into it
    # If firmware.tar.gz extracts into a 'firmware/' folder, copy its contents:
    if [ -d "$srcdir/firmware" ]; then
        cp -r "$srcdir/firmware"/* "$pkgdir/lib/firmware/postmarketos/"
    else
        # Fallback if the tarball extracts files directly
        cp -r "$srcdir"/* "$pkgdir/lib/firmware/postmarketos/"
    fi
}

sha512sums="
6cd1eaaa1c5642c3ba1fc6d70a5a2ec37deb899a09da4018b01a090bbae951579f2b89c6dd4d3e2f290d56172a0590f8a4884de4f4c03b30e08c2a3bc5230403  firmware.tar.gz
"
