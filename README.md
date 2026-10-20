Github action for installing MOSEK distro. This will install MOSEK in `/opt` or `C:/Program Files` or a similar place. 

It is possible to apply this action multiple times to install multiple MOSEK versions or distros.

Please note that this does NOT install a license. The user needs to ensure that a license is available when actually running MOSEK.

Action inputs (all optional):
- `version`. By default the latest stable release is chosen. This can be overridden by specifying a major/minor version
  as `X.Y` (in which case the latest build will be fetched) or the full version as `X.Y.Z`.
- `distro`. By default the correct distro for the platform will be detected. Otherwise, valid choices are: linux64x86',
  'linuxaarch64', 'win64x86', 'osxaarch64' and 'auto'"

Action outputs:
- `mosekbase`: The base installation directory, where the `mosek` folder is located.
- `mosekbindir`: The directory containing binaries and libraries
- `mosekdistro`: The distro name installed
- `version3`: The full version if the distro installed
- `version2`: The major/minor version if the distro installed.
