# Noctavo stations

Noctavo is a music player with an internet radio directory. The station list comes from the community database [radio-browser.info](https://www.radio-browser.info/); Noctavo does not host or re-broadcast any stream.

## Report a station or ask for removal

Broadcasters and listeners: [open an issue](https://github.com/ant2ric/noctavo-stations/issues/new) with the station name and, for removal requests, how you are connected to the station. Stations are hidden from the app on request.

## How removal works

`blocked_stations.json` is read by the app each time it starts. A station is hidden when it matches any entry:

- `ids`: the station's radio-browser UUID
- `names`: the exact station name (not case sensitive)
- `urlContains`: any part of the stream address, for example `example.com` to hide every stream from that site