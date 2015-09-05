# APK Crawler
APK Crawler is a tool to automatically retrieve APKs from various internet sources

## Usage
### Default
Fetches all APKs for all applications supported by Open GApps
```sh
python apkcrawler.py
```
### Specific
Fetches app APKs for specified applications supported by Open GApps using their [`.gapps-config` codename](https://github.com/opengapps/opengapps/wiki/Advanced-Features-and-Options#include-and-exclude-google-applications)
```sh
python apkcrawler.py drive docs slides sheets
```
### Inline
APK Crawler emits the downloaded filename so it can be used inline
```sh
./add_sourceapp.sh $(python apkcrawler.py drive docs slides sheets)
```

## Supported Sites
- [APK Mirror](http://apkmirror.com)
- ~~Google Play~~ (Not yet added)

## Requirements
- [python (make sure you have Python 2 (for now) or it won't work!)](https://www.python.org/downloads/)
- [requests](https://pypi.python.org/pypi/requests)
- [beautifulsoup4](https://pypi.python.org/pypi/beautifulsoup4/)
- [html5lib](https://pypi.python.org/pypi/html5lib)

## Installation
```sh
pip install requests beautifulsoup4 html5lib
```

## Known Issues
- There needs to be a way to grab an older version of an application as the current version (e.g. Current WebView on APK Mirror is the beta version)
