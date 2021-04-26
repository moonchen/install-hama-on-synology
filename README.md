# install-hama-on-synology
A way to install HAMA on Synology Plex

Work in progress.
```bash
sudo bash
cd /tmp
ln -s /volume1/Plex/Library/Application Support/Plex Media Server/ pms
mkdir -p 'pms/Scanners/Series'
wget -O 'pms/Scanners/Series/Absolute Series Scanner.py' https://raw.githubusercontent.com/ZeroQI/Absolute-Series-Scanner/master/Scanners/Series/Absolute%20Series%20Scanner.py
chown -R plex:users 'pms/Scanners'
chmod 775 -R 'pms/Scanners'

wget -O 'pms/Plug-ins/master.zip' https://github.com/ZeroQI/Hama.bundle/archive/master.zip
7z x -o'pms/Plug-ins/' 'pms/Plug-ins/master.zip' 
mv 'pms/Plug-ins/Hama.bundle-master' 'pms/Plug-ins/Hama.bundle'
rm 'pms/Plug-ins/master.zip'
chown -R plex:users 'pms/Plug-ins'
chmod 775 -R 'pms/Plug-ins'

wget -O 'pms/Plug-in.Support.folders.zip' https://github.com/ZeroQI/Hama.bundle/releases/download/v1.0/Plug-in.Support.folders.zip
7z x -o'pms/' 'pms/Plug-in.Support.folders.zip'
rm 'pms/Plug-in.Support.folders.zip'
chown -R plex:users 'pms/Plug-in Support'
chmod 775 -R 'pms/Plug-in Support'
```
