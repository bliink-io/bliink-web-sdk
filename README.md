# BLIINK Web SDK

BLIINK Web SDK is a javascript library for loading BLIINK in-image ads unit in publishers website images tags

## Table of Contents

* [Installation](#installation)
* [Load Ad](#load-ad)
* [Testing](#testing)

## Installation

### HTML

Place this code before `</html>` tag in your web page to initialize `BLIINK Web SDK` and call for and ad

Don't forgot to replace parameters between `[ ]` with your own IDs provided by us

```
<!-- BLIINK -->
<script type="text/javascript" charset="utf-8">
  var BLIINK_CACHEBUSTER = Math.round(new Date().getTime() / 1000);
  var BLIINK_PROTOCOL = (document.location.protocol === 'http:') ? 'http' : 'https'
  var BLIINK_MASTERTAG_URL = BLIINK_PROTOCOL + '://tag.bliink.io/library.min.js?cb=' + BLIINK_CACHEBUSTER
  document.write('\x3Cscript type="text/javascript" src="' + BLIINK_MASTERTAG_URL + '">\x3C/script>')
</script>
<script type="text/javascript" charset="utf-8">
  BLIINK.loadAd({networkId: [YOUR_NETWORK_ID], siteId: [YOUR_SITE_ID], tagId: [YOUR_TAG_ID]})
</script>
<!-- /BLIINK -->
```

### NPM package

> Coming soon

## Load Ad

This method automatically search for advertisable images in your web page, call and show a matching ad

```
BLIINK.loadAd({networkId: [YOUR_NETWORK_ID], siteId: [YOUR_SITE_ID], tagId: [YOUR_TAG_ID]})
```

## Testing

To verify that your integration is working properly, add the `testMode` parameter to `loadAd` config

```
BLIINK.loadAd({networkId: [YOUR_NETWORK_ID], siteId: [YOUR_SITE_ID], tagId: [YOUR_TAG_ID], testMode: 1})
```
