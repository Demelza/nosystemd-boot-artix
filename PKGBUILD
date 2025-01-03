# Maintainer: Neko <demeruza@yahoo.fr>
# Maintainer: Christian Hesse <mail@eworm.de>

pkgbase='systemd'
pkgname='nosystemd-boot-artix'
_tag='257.1'
# Upstream versioning is incompatible with pacman's version comparisons, one
# way or another. So we replace dashes and tildes with the empty string to
# make sure pacman's version comparing does the right thing for rc versions:
pkgver="${_tag/[-~]/}"
pkgrel=1
arch=('x86_64')
license=('LGPL-2.1-or-later')
url='https://www.github.com/systemd/systemd'
makedepends=('acl' 'cryptsetup' 'docbook-xsl' 'gperf' 'lz4' 'xz' 'pam' 'libelf'
             'intltool' 'iptables' 'kmod' 'libarchive' 'libcap' 'libidn2' 'libgcrypt'
             'libmicrohttpd' 'libxcrypt' 'libxslt' 'util-linux' 'linux-api-headers'
             'python-jinja' 'python-lxml' 'quota-tools' 'shadow' 'git'
             'meson' 'libseccomp' 'pcre2' 'audit' 'kexec-tools' 'libxkbcommon'
             'bash-completion' 'p11-kit' 'libfido2' 'tpm2-tss' 'rsync'
             'bpf' 'libbpf' 'clang' 'llvm' 'curl' 'gnutls' 'python-pyelftools'
             'libpwquality' 'qrencode' 'lib32-gcc-libs' 'python-pefile')
conflicts=("mkinitcpio<38-1")
validpgpkeys=('63CDA1E5D3FC22B998D20DD6327F26951A015CC4'  # Lennart Poettering <lennart@poettering.net>
              'A9EA9081724FFAE0484C35A1A81CEA22BC8C7E2E'  # Luca Boccassi <luca.boccassi@gmail.com>
              '9A774DB5DB996C154EBBFBFDA0099A18E29326E1'  # Yu Watanabe <watanabe.yu+github@gmail.com>
              '5C251B5FC54EB2F80F407AAAC54CA336CFEB557E') # Zbigniew Jędrzejewski-Szmek <zbyszek@in.waw.pl>
source=("git+https://github.com/systemd/systemd#tag=v${_tag}?signed"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/0001-Use-Arch-Linux-device-access-groups.patch"
        # bootloader files
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/arch.conf"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/loader.conf?ref_type=heads"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/splash-arch.bmp"
        # pam configuration
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/systemd-user.pam"
        # pacman / libalpm hooks
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/systemd-hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/20-systemd-sysusers.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-binfmt.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-catalog.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-daemon-reload-system.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-daemon-reload-user.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-hwdb.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-restart-marked.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-sysctl.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-tmpfiles.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-udev-reload.hook"
        "https://gitlab.archlinux.org/archlinux/packaging/packages/systemd/-/raw/main/30-systemd-update.hook")
sha512sums=('53b14cfadf301a44fdfcaa2fe4b9d2371c85581544093b88e5afcee4e45c5bd8668aaae9dd6663363c24f3b610f9b0d6eb61f00df71d588bce8f6264424203e4'
            '78065bde708118b7d6e4ed492e096c763e4679a1c54bd98750d5d609d8cc2f1373023f308880f14fc923ae7f9fea34824917ef884c0f996b1f43d08ef022c0fb'
            '61032d29241b74a0f28446f8cf1be0e8ec46d0847a61dadb2a4f096e8686d5f57fe5c72bcf386003f6520bc4b5856c32d63bf3efe7eb0bc0deefc9f68159e648'
            'c416e2121df83067376bcaacb58c05b01990f4614ad9de657d74b6da3efa441af251d13bf21e3f0f71ddcb4c9ea658b81da3d915667dc5c309c87ec32a1cb5a5'
            '5a1d78b5170da5abe3d18fdf9f2c3a4d78f15ba7d1ee9ec2708c4c9c2e28973469bc19386f70b3cf32ffafbe4fcc4303e5ebbd6d5187a1df3314ae0965b25e75'
            'b90c99d768dc2a4f020ba854edf45ccf1b86a09d2f66e475de21fe589ff7e32c33ef4aa0876d7f1864491488fd7edb2682fc0d68e83a6d4890a0778dc2d6fe19'
            '81baa1ae439b0f4d1f09371a82c02db06a97a4fc35545fc2654f7905b4422fc8cf085f70304919a4323f39e662df1e05aa8d977d1dde73507527abe3072c386b'
            '299dcc7094ce53474521356647bdd2fb069731c08d14a872a425412fcd72da840727a23664b12d95465bf313e8e8297da31259508d1c62cc2dcea596160e21c5'
            '0d6bc3d928cfafe4e4e0bc04dbb95c5d2b078573e4f9e0576e7f53a8fab08a7077202f575d74a3960248c4904b5f7f0661bf17dbe163c524ab51dd30e3cb80f7'
            '2b50b25e8680878f7974fa9d519df7e141ca11c4bfe84a92a5d01bb193f034b1726ea05b3c0030bad1fbda8dbb78bf1dc7b73859053581b55ba813c39b27d9dc'
            'a436d3f5126c6c0d6b58c6865e7bd38dbfbfb7babe017eeecb5e9d162c21902cbf4e0a68cf3ac2f99815106f9fa003b075bd2b4eb5d16333fa913df6e2f3e32a'
            '190112e38d5a5c0ca91b89cd58f95595262a551530a16546e1d84700fc9644aa2ca677953ffff655261e8a7bff6e6af4e431424df5f13c00bc90b77c421bc32d'
            'a1661ab946c6cd7d3c6251a2a9fd68afe231db58ce33c92c42594aedb5629be8f299ba08a34713327b373a3badd1554a150343d8d3e5dfb102999c281bd49154'
            'f6b154fdc612916d7788720cf703e34255b43ba2d19413de5f3f63f07508f4ce561ca138f987c2118c7128e1dfb01976b0ac7d5efee4d9ebaadd180e70fa013e'
            '9426829605bbb9e65002437e02ed54e35c20fdf94706770a3dc1049da634147906d6b98bf7f5e7516c84068396a12c6feaf72f92b51bdf19715e0f64620319de'
            'da7a97d5d3701c70dd5388b0440da39006ee4991ce174777931fea2aa8c90846a622b2b911f02ae4d5fffb92680d9a7e211c308f0f99c04896278e2ee0d9a4dc'
            'a50d202a9c2e91a4450b45c227b295e1840cc99a5e545715d69c8af789ea3dd95a03a30f050d52855cabdc9183d4688c1b534eaa755ebe93616f9d192a855ee3'
            '825b9dd0167c072ba62cabe0677e7cd20f2b4b850328022540f122689d8b25315005fa98ce867cf6e7460b2b26df16b88bb3b5c9ebf721746dce4e2271af7b97')

_meson_version="${pkgver}-${pkgrel}"
_meson_vcs_tag='false'
_meson_mode='release'
_meson_compile=()
_meson_install=()

if ((_systemd_UPSTREAM)); then
  _meson_version="${pkgver}"
  _meson_mode='developer'
  pkgname+=('systemd-tests')
  if ((_systemd_QUIET)); then
    _meson_install=('--quiet')
  else
    _meson_compile=('--verbose')
  fi
fi

_backports=(
)

_reverts=(
)

_efiarch=x64
_targets=(
    bootctl
#    man/bootctl.1
#    man/kernel-install.8
    "src/boot/efi/linux$_efiarch."{efi,elf}".stub"
    "src/boot/efi/systemd-boot$_efiarch.efi"
    "src/shared/libsystemd-shared-$_tag-$pkgrel.so"
  )

prepare() {
  cd "${pkgbase}"

  # add upstream repository for cherry-picking
  git remote add -f upstream ../systemd

  local _c _l
  for _c in "${_backports[@]}"; do
    if [[ "${_c}" == *..* ]]; then _l='--reverse'; else _l='--max-count=1'; fi
    git log --oneline "${_l}" "${_c}"
    git cherry-pick --mainline 1 --no-commit "${_c}"
  done
  for _c in "${_reverts[@]}"; do
    if [[ "${_c}" == *..* ]]; then _l='--reverse'; else _l='--max-count=1'; fi
    git log --oneline "${_l}" "${_c}"
    git revert --mainline 1 --no-commit "${_c}"
  done

  # Replace cdrom/dialout/tape groups with optical/uucp/storage
  patch -Np1 -i ../0001-Use-Arch-Linux-device-access-groups.patch
}

build() {
  local _timeservers=({0..3}.arch.pool.ntp.org)
  local _nameservers=(
    # We use these public name services, ordered by their privacy policy (hopefully):
    #  * Cloudflare (https://1.1.1.1/)
    #  * Quad9 (https://www.quad9.net/)
    #  * Google (https://developers.google.com/speed/public-dns/)
    '1.1.1.1#cloudflare-dns.com'
    '9.9.9.9#dns.quad9.net'
    '8.8.8.8#dns.google'
    '2606:4700:4700::1111#cloudflare-dns.com'
    '2620:fe::9#dns.quad9.net'
    '2001:4860:4860::8888#dns.google'
  )

  local _meson_options=(
    -Dversion-tag="${_meson_version}-arch"
    -Dvcs-tag="${_meson_vcs_tag}"
    -Dshared-lib-tag="${_meson_version}"
    -Dmode="${_meson_mode}"

    -Dapparmor=disabled
    -Dbootloader=enabled
    -Dxenctrl=disabled
    -Dbpf-framework=enabled
    -Dima=false
    -Dinstall-tests=true
    -Dlibidn2=enabled
    -Dlz4=enabled
    -Dman=enabled
    -Dnscd=false
    -Dselinux=disabled
    -Dsshdprivsepdir=/usr/share/empty.sshd

    # We disable DNSSEC by default, it still causes trouble:
    # https://github.com/systemd/systemd/issues/10579

    -Ddbuspolicydir=/usr/share/dbus-1/system.d
    -Ddefault-dnssec=no
    -Ddefault-kill-user-processes=false
    -Ddefault-locale='C.UTF-8'
    -Dlocalegen-path=/usr/bin/locale-gen
    -Ddns-over-tls=openssl
    -Dfallback-hostname='archlinux'
    -Dnologin-path=/usr/bin/nologin
    -Dntp-servers="${_timeservers[*]}"
    -Ddns-servers="${_nameservers[*]}"
    -Drpmmacrosdir=no
    -Dsysvinit-path=
    -Dsysvrcnd-path=

    -Dsbat-distro='arch'
    -Dsbat-distro-summary='Arch Linux'
    -Dsbat-distro-pkgname="${pkgname}"
    -Dsbat-distro-version="${pkgver}"
    -Dsbat-distro-url="https://archlinux.org/packages/core/x86_64/${pkgname}/"
  )

  arch-meson "${pkgbase}" build "${_meson_options[@]}" $MESON_EXTRA_CONFIGURE_OPTIONS

  meson compile -C build "${_meson_compile[@]}"
}

check() {
  meson test -C build --print-errorlogs
}

package() {
  install -Dm755 build/bootctl "$pkgdir/usr/bin/bootctl"

  install -d "$pkgdir/usr/lib/systemd/boot/efi"
  cp build/src/boot/{linux${_efiarch}.{efi,elf}.stub,systemd-boot${_efiarch}.efi}  "$pkgdir/usr/lib/systemd/boot/efi"

  install -Dm755 build/kernel-install "$pkgdir/usr/bin/kernel-install"

  install -Dm755 build/src/shared/libsystemd-shared-$_tag-$pkgrel.so "$pkgdir/usr/lib/libsystemd-shared-$_tag-$pkgrel.so"
}
