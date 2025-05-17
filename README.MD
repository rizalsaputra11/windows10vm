<h1 align="center">Windows 10 in Docker</h1>

## Installation
1. Clone the repository or download:
`git clone https://github.com/hopingboyz/windows10vm`

3. go to directory:
`cd windows10vm`

3. Run this impotent :
`docker build -t windows10-vm .`

5. Run Windows 10 in Docker:
`docker run -it --rm \
  --device /dev/kvm \
  -p 6080:6080 \
  -p 3389:3389 \
  -v windows_data:/data \
  -v windows_iso:/iso \
  windows10-vm`
