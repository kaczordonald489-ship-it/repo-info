## `swift:windowsservercore-ltsc2022`

```console
$ docker pull swift@sha256:cb3ff58e95893abd1052a84b8b2f414d6b09b18463143cb393bd8f30b98d1346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `swift:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull swift@sha256:c4397fa2345edd71148bd6efee9066f22d370f8807dbe30a8f103eac1fe886e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6220527980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84156288a6fb6d4bfcd777837ee593ec6acad24296a5e2321581217a9bced5df`
-	Default Command: `["powershell.exe","-nologo","-ExecutionPolicy","Bypass"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 23:13:08 GMT
RUN cmd /S /C #(nop)  LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 13 Jan 2026 23:13:08 GMT
RUN cmd /S /C #(nop)  LABEL description=Docker Container for the Swift programming language
# Tue, 13 Jan 2026 23:13:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:13:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Jan 2026 23:13:10 GMT
ARG GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe
# Tue, 13 Jan 2026 23:13:11 GMT
ARG GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
# Tue, 13 Jan 2026 23:14:03 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:GIT});                   Invoke-WebRequest -Uri ${env:GIT} -OutFile git.exe;                             Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:GIT_SHA256});     $Hash = Get-FileHash git.exe -Algorithm sha256;                                 if ($Hash.Hash -eq ${env:GIT_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing git ... ';                                    $Process =                                                                          Start-Process git.exe -Wait -PassThru -NoNewWindow -ArgumentList @(               '/SP-',                                                                         '/VERYSILENT',                                                                  '/SUPPRESSMSGBOXES',                                                            '/NOCANCEL',                                                                    '/NORESTART',                                                                   '/CLOSEAPPLICATIONS',                                                           '/FORCECLOSEAPPLICATIONS',                                                      '/NOICONS',                                                                     '/COMPONENTS="gitlfs"',                                                         '/EditorOption=VIM',                                                            '/PathOption=Cmd',                                                              '/SSHOption=OpenSSH',                                                           '/CURLOption=WinSSL',                                                           '/UseCredentialManager=Enabled',                                                '/EnableSymlinks=Enabled',                                                      '/EnableFSMonitor=Enabled'                                                    );                                                                          if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force git.exe;                                                     Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 13 Jan 2026 23:14:04 GMT
ARG PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe
# Tue, 13 Jan 2026 23:14:04 GMT
ARG PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B
# Tue, 13 Jan 2026 23:14:39 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:PY310});                 Invoke-WebRequest -Uri ${env:PY310} -OutFile python-3.10.11-amd64.exe;          Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:PY310_SHA256});    $Hash = Get-FileHash python-3.10.11-amd64.exe -Algorithm sha256;                if ($Hash.Hash -eq ${env:PY310_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Python ... ';                                 $Process =                                                                          Start-Process python-3.10.11-amd64.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            'AssociateFiles=0',                                                             'Include_doc=0',                                                                'Include_debug=0',                                                              'Include_lib=1',                                                                'Include_tcltk=0',                                                              'Include_test=0',                                                               'InstallAllUsers=1',                                                            'InstallLauncherAllUsers=0',                                                    'PrependPath=1',                                                                '/quiet'                                                                      );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force python-3.10.11-amd64.exe;                                    Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 13 Jan 2026 23:14:40 GMT
ARG VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe
# Tue, 13 Jan 2026 23:14:40 GMT
ARG VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
# Tue, 13 Jan 2026 23:24:02 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:VSB});                   Invoke-WebRequest -Uri ${env:VSB} -OutFile vs_buildtools.exe;                   Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:VSB_SHA256});     $Hash = Get-FileHash vs_buildtools.exe -Algorithm sha256;                       if ($Hash.Hash -eq ${env:VSB_SHA256}) {                                           Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Visual Studio Build Tools ... ';              $Process =                                                                          Start-Process vs_buildtools.exe -Wait -PassThru -NoNewWindow -ArgumentList @(           '--quiet',                                                                      '--wait',                                                                       '--norestart',                                                                  '--nocache',                                                                    '--add', 'Microsoft.VisualStudio.Component.Windows11SDK.22000',                 '--add', 'Microsoft.VisualStudio.Component.VC.Tools.x86.x64'                  );                                                                          if ($Process.ExitCode -eq 0 -or $Process.ExitCode -eq 3010) {                     Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force vs_buildtools.exe;                                           Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 13 Jan 2026 23:24:03 GMT
ARG SWIFT=https://download.swift.org/swift-6.2.3-release/windows10/swift-6.2.3-RELEASE/swift-6.2.3-RELEASE-windows10.exe
# Tue, 13 Jan 2026 23:24:04 GMT
ARG SWIFT_SHA256=10A4D887C383BEC128F3F11B8CAAAE8FBD0D13FF10CC9844C578B6560F1F3E77
# Tue, 13 Jan 2026 23:27:38 GMT
# ARGS: GIT=https://github.com/git-for-windows/git/releases/download/v2.42.0.windows.2/Git-2.42.0.2-64-bit.exe GIT_SHA256=BD9B41641A258FD16D99BEECEC66132160331D685DFB4C714CEA2BCC78D63BDB PY310=https://www.python.org/ftp/python/3.10.11/python-3.10.11-amd64.exe PY310_SHA256=D8DEDE5005564B408BA50317108B765ED9C3C510342A598F9FD42681CBE0648B SWIFT=https://download.swift.org/swift-6.2.3-release/windows10/swift-6.2.3-RELEASE/swift-6.2.3-RELEASE-windows10.exe SWIFT_SHA256=10A4D887C383BEC128F3F11B8CAAAE8FBD0D13FF10CC9844C578B6560F1F3E77 VSB=https://download.visualstudio.microsoft.com/download/pr/5536698c-711c-4834-876f-2817d31a2ef2/c792bdb0fd46155de19955269cac85d52c4c63c23db2cf43d96b9390146f9390/vs_BuildTools.exe VSB_SHA256=C792BDB0FD46155DE19955269CAC85D52C4C63C23DB2CF43D96B9390146F9390
RUN Write-Host -NoNewLine ('Downloading {0} ... ' -f ${env:SWIFT});                 Invoke-WebRequest -Uri ${env:SWIFT} -OutFile installer.exe;                     Write-Host '✓';                                                                 Write-Host -NoNewLine ('Verifying SHA256 ({0}) ... ' -f ${env:SWIFT_SHA256});     $Hash = Get-FileHash installer.exe -Algorithm sha256;                           if ($Hash.Hash -eq ${env:SWIFT_SHA256}) {                                         Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Hash.Hash);                                           exit 1;                                                                       }                                                                               Write-Host -NoNewLine 'Installing Swift ... ';                                  $Process =                                                                          Start-Process installer.exe -Wait -PassThru -NoNewWindow -ArgumentList @(            '/quiet',                                                                       '/norestart'                                                                  );                                                                         if ($Process.ExitCode -eq 0) {                                                    Write-Host '✓';                                                               } else {                                                                          Write-Host ('✘ ({0})' -f $Process.ExitCode);                                    exit 1;                                                                       }                                                                               Remove-Item -Force installer.exe;                                               Remove-Item -ErrorAction SilentlyContinue -Force -Recurse ${env:TEMP}\*
# Tue, 13 Jan 2026 23:27:39 GMT
CMD ["powershell.exe" "-nologo" "-ExecutionPolicy" "Bypass"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993e816c71561843a433bd25d318dcc6ef44a88ece838ab68df43a6f44aefce5`  
		Last Modified: Tue, 13 Jan 2026 23:28:07 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52024721d6ab11f12b8ea6485c8c1e46f8bb46ee0252fb5a4d1a647db987d2ac`  
		Last Modified: Tue, 13 Jan 2026 23:28:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567d9e580611ae9b710418fb0e22e6bc27873dfe902c279a831bee61fc16ffde`  
		Last Modified: Tue, 13 Jan 2026 23:28:05 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd717a182a513d633c6d008233467e40c60d98e1df9498f2580638d71a9f3295`  
		Last Modified: Tue, 13 Jan 2026 23:28:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e082a92e66ebf55db666559e6de4edd02ac79163b92a01f518a6c371615e83`  
		Last Modified: Tue, 13 Jan 2026 23:28:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7d8bf3c2c08a37a9d074da97aa84e3766cf4725a8f585789cdc325f2794728`  
		Last Modified: Tue, 13 Jan 2026 23:28:00 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353681379dd6af7b81efc47d32521527c64542befd3d550a16ac8cd3d57902d2`  
		Last Modified: Tue, 13 Jan 2026 23:28:22 GMT  
		Size: 150.4 MB (150448366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5559369f4c1fa2edf76acc27b2901a6c63306240d913291eb9dfeb8d3728af`  
		Last Modified: Tue, 13 Jan 2026 23:27:59 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d81a8463a032cc85129865328522304c8e6c870c0a08d849a2f7146719c5822`  
		Last Modified: Tue, 13 Jan 2026 23:27:59 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4b01a01e46b2c962f45c78695022e87c5fc32a1e4995503b40680683bdd5de`  
		Last Modified: Tue, 13 Jan 2026 23:28:03 GMT  
		Size: 46.3 MB (46287155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff771b9f77c1ff6a010f46ec372245936f8935cf9d2e9d385b1ec25927550ed`  
		Last Modified: Tue, 13 Jan 2026 23:27:57 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3324c068535df3f031e160a8ad9520495e5f34dc3169f88cfb53012bb7a9878a`  
		Last Modified: Tue, 13 Jan 2026 23:27:57 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3feb091ecd1aee3deecead551b6f153dade1d3927398f70cf36a06b5ef6efe26`  
		Last Modified: Tue, 13 Jan 2026 23:30:37 GMT  
		Size: 1.7 GB (1689362629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6346de48ffd5c0aaa9db9eff62cad27bd7385c2b1cbca0a7e0b2d985b1588ea5`  
		Last Modified: Tue, 13 Jan 2026 23:27:56 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a690469ad269aac6e7a6f8b2e252b49301f0d8d9612ed48d9cf4c7b550a1d0a`  
		Last Modified: Tue, 13 Jan 2026 23:27:56 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510a964997ef7337fe6c87a75ba82925eb623944ac99eed125ca4cd55ade5574`  
		Last Modified: Tue, 13 Jan 2026 23:31:28 GMT  
		Size: 2.5 GB (2498753571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2063a3f9d2a22e5c3e4ba66cdf0d83411a95ecb738e4b8f1813a9ab212503763`  
		Last Modified: Tue, 13 Jan 2026 23:27:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
